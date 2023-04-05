<template>
  <h1>Posts List</h1>
  <div v-for="post in posts" :key="post.id">
    <SinglePost :post="post"></SinglePost>
  </div>
</template>

<script>
import SinglePost from './SinglePost'
import { onMounted, onUnmounted, onUpdated } from 'vue'
export default {
    components: { SinglePost },
    props:["posts"],
    setup() {
    }
}
</script>

<style>

</style>