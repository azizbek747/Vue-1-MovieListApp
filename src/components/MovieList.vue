<template>
  <ul class="list-group">
    <MovieListItem />
    <MovieListItem />
    <MovieListItem />
  </ul>
</template>

<script>
  import MovieListItem from "./MovieListItem.vue"
  export default {
    components: {
      MovieListItem
    }
  }
</script>

<style scoped>

</style>