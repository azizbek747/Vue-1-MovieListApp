<template>
  <ul class="list-group">
    <MovieListItem v-for="movie in movies" :key="movie.name" :movie="movie" />
    
  </ul>
</template>

<script>
  import MovieListItem from "./MovieListItem.vue"
  export default {
    data: () => ({
     movies: [
      {
        name: "Omar",
        viewers: 6098,
        like: true,
        favourite: false
      },
      {
        name: "Empire of Osman",
        viewers: 6098,
        like: false,
        favourite: true
      },
      {
        name: "Ertugrul",
        viewers: 6098,
        like: true,
        favourite: false
      },
     ] 
    }),
    components: {
      MovieListItem
    }
  }
</script>

<style scoped>

</style>