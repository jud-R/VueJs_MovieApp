<template>
  <div id="app">
    <search-form @search="changeMovieResults">
    </search-form>
    <movie-list :movies="movies"></movie-list>
  </div>
</template>

<script>
import SearchForm from './components/SearchForm'
import MovieList from './components/MovieList'

export default {
  name: 'app',
  components: {
    SearchForm,
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
  @media screen and (max-width: 600px) {
  padding: 1rem 2rem;
}
}
</style>
