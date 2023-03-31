<template>
  <div class="home">
    <PostsList :posts="posts"></PostsList>
  </div>
</template>

<script>
import { ref } from 'vue'
import PostsList from '../components/PostsList'
// @ is an alias to /src


export default {
  components: { PostsList },
  setup() {
    let posts = ref([
      
    ])
    return {posts}
  }
}
</script>
