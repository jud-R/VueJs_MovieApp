<template>
  <div id="app">
    <search @search="changeMovieResult"></search>
  </div>
</template>

<script>
import Search from './components/Search'

export default {
  name: 'app',
  components: {
    Search
  },
  data () {
    return {
      movies: []
    }
  },
  method: {
    changeMovieResult (results) {
      this.movies = results
    }
  }
}
</script>
