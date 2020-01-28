<template>
      <li>
        <img :src="movie.Poster"/>
        {{movie.Year}}
        {{movie.Title}}
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