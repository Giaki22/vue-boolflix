<template>
    <main>
        <h2>FILMS</h2>
        <ul>
            <li v-for="(film, i) in data.resultsFilms" :key="i">
                <ResultFilmCard :film="film"></ResultFilmCard>
            </li>
        </ul>
    </main>
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