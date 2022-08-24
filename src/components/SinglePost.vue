<template>
    <div>
        <h2>{{ post.title }}</h2>
        <p>{{ cutPostBody }}</p>
    </div>
</template>

<script>
import { computed } from 'vue'
export default {
    props: ['post'],

    setup(props) {

        let cutPostBody = computed(()=>{
            return props.post.body.substring(0,5)+'...';
        })

        return { cutPostBody }
    }

}
</script>

<style>

</style>