<template>
  <div id="app">
    <search @search="changeMovieResults"></search>
    <movie-list :movies="movies"></movie-list>
  </div>
</template>

<script>
import Search from './components/Search'
import MovieList from './components/MovieList'

export default {
  name: 'app',
  components: {
    Search,
    MovieList
  },
  data () {
    return {
      movies: []
    }
  },
  methods: {
    changeMovieResults (results) {
      this.movies = results
    }
  }
}
</script>
<style>
:root {
  --violet-darkest: #5F3C77;
  --orange-light: #EA5B23;
  --white: #20221F;
  --grey-light: #bdb8b8;
  --yellow: #E3B044;
}
html {
  font-size: 62.5%;
}
body {
  font-family: 'Lato';
  font-weight: 400;
}
</style>
<style lang="scss" scoped>
#app {
  min-height: 100vh;
  padding: 2rem 4rem;
  background-color: var(--violet-darkest);
}
</style>
