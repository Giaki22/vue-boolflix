<template>
  <ul>
      <li v-for="(film, i) in data.resultsFilms" :key="i">
        <ResultFilmCard :film="film"></ResultFilmCard>
      </li>
  </ul>
</template>

<script>
import data from '../../assets/shared/data.js'
import ResultFilmCard from '../Atoms/ResultFilmCard.vue'

export default {
name: 'FilmsContainer',
    data() {
        return {
            data
        };
    },
    components: { ResultFilmCard }
}
</script>

<style lang="scss" scoped>
ul{
    list-style: none;
    display: flex;
    li{
        width: calc(100% / 6);
    }
}
</style>