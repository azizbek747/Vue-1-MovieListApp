<template>
  <div class="container">
    <Box>
      <AppInfo :moviesCount="movies.length" :favouriteMoviesCount="movies.filter(m => m.favourite).length" />
    </Box> 
    <Box>
      <SearchPanel />
      <AppFilter />
    </Box>
    <Box>
      <MovieList :movies="movies" @onToggle="ontoggle" />
    </Box>
    <Box>
      <AddForm @add-movie="movies.push($event)" />
    </Box>
  </div>
</template>

<script>
import AppInfo from "./components/AppInfo.vue";
import SearchPanel from "./components/SearchPanel.vue";
import AppFilter from "./components/AppFilter.vue";
import MovieList from "./components/MovieList.vue";
import AddForm from "./components/AddForm.vue";
import Box from "./components/Box.vue";

export default {
  components: {
    AppInfo,
    SearchPanel,
    AppFilter,
    MovieList,
    AddForm,
    Box,
  },
  data: () => ({
    movies: [
      {
        id: 1,
        name: "Omar",
        viewers: 6098,
        like: true,
        favourite: false
      },
      {
        id: 2,
        name: "Empire of Osman",
        viewers: 6098,
        like: false,
        favourite: true
      },
      {
        id: 3,
        name: "Ertugrul",
        viewers: 6098,
        like: true,
        favourite: false
      },
    ] 
  }),
  methods: {
    ontoggle({id, prop}) {
      this.movies = this.movies.map((movie) => {
        if (movie.id === id) {
          return { ...movie, [prop]: !movie[prop] };
        }
        return movie;
      });
    },
  },

};
</script>

<style >
body {
  font-family: monospace;
}
.container {
  max-width: 1080px;
  margin: 50px auto;
  
}
</style>
