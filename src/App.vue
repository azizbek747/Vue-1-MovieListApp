<template>
  <div class="container">
    <Box>
      <AppInfo />
    </Box>
    <Box>
      <SearchPanel />
      <AppFilter />
    </Box>
    <Box>
      <MovieList />
    </Box>
    <Box>
      <AddForm />
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
