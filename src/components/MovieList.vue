<template>
  <ul class="list-group">
    <MovieListItem v-for="movie in movies" :key="movie.name" :movie="movie" />
    
  </ul>
</template>

<script>
  import MovieListItem from "./MovieListItem.vue"
  export default {
    
    components: {
      MovieListItem
    },
    props: {
      movies: {
        type: Array,
        required: true
      }
    }
  }
</script>

<style scoped>

</style>