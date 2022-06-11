<template>
  <main>
      <div class="pic">
        <img :src="`https://image.tmdb.org/t/p/w780${film.poster_path}`" v-if="film.poster_path !== null">
        <img :src="`https://cdn1.iconfinder.com/data/icons/leto-files/64/leto_files-58-512.png`" v-if="film.poster_path == null">
      </div>
      <div class="info">
          <h1>{{film.title}}</h1>
          <h3>{{film.original_title}}</h3>
          <LangFlag :iso="film.original_language" v-if="(film.original_language !== undefined)"></LangFlag>
          <div class="stars">
              <i class="fa-solid fa-star" v-for="i in Math.ceil(film.vote_average / 2)" :key="i"></i>
          </div>
      </div>
  </main>
</template>

<script>
import LangFlag from 'vue-lang-code-flags';

export default {
    name: "ResultFilmCard",
    props: {
        film: Object
    },
    components: { LangFlag }
}
</script>

<style lang="scss" scoped>
main{
    .pic{
        img{
            width: 100%;
            aspect-ratio: 9/16;
        }
    }
    .stars{
        display: flex;
        flex-flow: row nowrap;
        gap: 2px;
        i{
            color: rgb(213, 193, 12);
        }
    }
}
</style>