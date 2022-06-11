<template>
  <ul>
      <li v-for="(serie, i) in data.resultsSeries" :key="i">
        <ResultSerieCard :serie="serie"></ResultSerieCard>
      </li>
  </ul>
</template>

<script>
import data from '../../assets/shared/data.js'
import ResultSerieCard from '../Atoms/ResultSerieCard.vue'

export default {
name: 'SeriesContainer',
    data() {
        return {
            data
        };
    },
    components: { ResultSerieCard }
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