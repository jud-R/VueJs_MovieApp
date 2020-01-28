<template>
  <ul>
      <movie-list-item
      v-for="movie in movies"
      :movie="movie"
      :key="movie.imdbID"></movie-list-item>
  </ul>
</template>

<script>

import MovieListItem from './MovieListItem'

export default {
  name: 'movie-list',
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

<style>
</style>
