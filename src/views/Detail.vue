<template>
    <div>
        <div v-if="post" class="post">
            <h2>{{post.title}}</h2>
            <p>{{post.body}}</p>
        </div>
        <div v-else>
            <Spinner></Spinner>
        </div>  
    </div>
</template>

<script>
import Spinner from '../components/Spinner'
import getPost from '../composables/getPost'
import { useRoute } from 'vue-router'

export default {
  components: { Spinner },
    props: ['id'],

    setup(props) {
        let route=useRoute();
        let { post, error, load }=getPost(route.params.id);
        load();
       
        return { post, error };
    }
}
</script>

<style>

</style>