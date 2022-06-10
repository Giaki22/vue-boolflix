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
    axios.get(`https://api.themoviedb.org/3/search/${this.data.type}?api_key=d6cee5e2b967b318798d59895632046d&query=${this.data.searchText}&language=${this.data.language}`)
        .then((reply) => {
            this.data.searchResults = reply.data;
        });
    }
}
}
</script>

<style>

</style>