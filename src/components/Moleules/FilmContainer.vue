<template>
  <ul>
      <li v-for="(film, i) in data.searchResults.results" :key="i">
        <ResultCard :film="film"></ResultCard>
      </li>
  </ul>
</template>

<script>
import data from '../../assets/shared/data.js'
import ResultCard from '../Atoms/ResultCard.vue'

export default {
name: 'FilmContainer',
    data() {
        return {
            data
        };
    },
    components: { ResultCard }
}
</script>

<style lang="scss" scoped>
ul{
    list-style: none;
    display: flex;
}
</style>