<template>
    <div>
        <h1>Post List</h1>
        <div v-for="post in posts" :key="post">
            <SinglePost :post="post"></SinglePost>
        </div>
    </div>
</template>

<script>
import SinglePost from './SinglePost'

export default {
  components: { SinglePost },
    props: ['posts'],
}
</script>

<style>

</style>