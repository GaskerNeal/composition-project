<template>

  <div class="home">
    <div v-if="error">
      {{ error }}
    </div>
    <div v-if="posts.length>0">
      <PostsList :posts="posts"></PostsList>
    </div>
    <div v-else>
      <Spinner></Spinner>
    </div>
  </div>
</template>

<script>
import Spinner from '../components/Spinner'
import { ref } from 'vue'
import PostsList from '../components/PostsList'
import getPosts from '../composable/getPosts'
// @ is an alias to /src


export default {
  components: {
    Spinner, PostsList },
  setup() {
    let {posts, error, load} = getPosts()
    load()
    return {posts, error}
  }
}
</script>
