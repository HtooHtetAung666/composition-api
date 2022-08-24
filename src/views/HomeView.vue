<template>
  <div class="home">
    <PostList :posts="posts"></PostList>
  </div>
</template>

<script>
import PostList from '../components/PostList'
import { ref } from 'vue'

export default {
  components: { PostList },  

  setup() {
    let posts = ref([
      {title: 'post 1', body: 'lorem ipsum 1'},
      {title: 'post 2', body: 'lorem ipsum 2'}
    ])

    return { posts }
  }
}
</script>
