<template>
    <main>
        <h2>SERIE TV</h2>
        <ul>
            <li v-for="(serie, i) in data.resultsSeries" :key="i">
                <ResultSerieCard :serie="serie"></ResultSerieCard>
            </li>
        </ul>
    </main>
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
main{
    h2{
        color: white;
    }
    ul{
        list-style: none;
        display: flex;
        overflow: auto;
        li{
            width: calc(100% / 6);
            display: flex;
            flex-shrink: 0;
        }
    }
}
</style>