<template>
  <router-link :to="{name:'Detail',params:{id:post.id}}">
    <h2>{{ post.title }}</h2>
  </router-link>
  <p>{{ post.body }}</p>
</template>

<script>
export default {
    props:["post"],
}
</script>

<style>

</style>