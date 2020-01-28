<template>
      <li>
        <img :src="movie.Poster"/>
        {{movie.Year}}
        {{movie.Title}}
        <a :href="`https://www.imdb.com/title/${movie.imdbID}`" target="_blank">More</a>
      </li>
</template>

<script>
export default {
  name: 'movie-list-item',
  props: {
    movie: {
      type: Object,
      required: true
    }
  }
}
</script>

<style>
</style>
