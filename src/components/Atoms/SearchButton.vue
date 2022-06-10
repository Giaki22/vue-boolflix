<template>
  <button @click="searchFilm()">Search</button>
</template>

<script>
import axios from 'axios';
import data from '../../assets/shared/data.js'

export default {
name: 'SearchButtons',
data() {
    return {
        data
    }
},
methods: {
    searchFilm() {
    axios.get(`https://api.themoviedb.org/3/search/multi?api_key=d6cee5e2b967b318798d59895632046d&query=${this.data.searchText}&language=${this.data.language}`)
        .then((reply) => {
            this.data.resultsFilms = [];
            this.data.resultsSeries = [];
            this.data.searchResults = reply.data;
            console.log(data.searchResults)
            data.searchResults.results.forEach((obj) => this.sortType(obj))
        });
    },
    sortType(obj) {
        if (obj.media_type == "movie") {
            this.data.resultsFilms.push(obj);
        } else if (obj.media_type == "tv") {
            this.data.resultsSeries.push(obj);
        }
    }
}
}
</script>

<style>

</style>