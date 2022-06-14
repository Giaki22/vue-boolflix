<template>
  <main>
      <div class="pic">
        <img :src="`https://image.tmdb.org/t/p/w780${film.poster_path}`" v-if="film.poster_path !== null">
        <img :src="`https://cdn1.iconfinder.com/data/icons/leto-files/64/leto_files-58-512.png`" v-if="film.poster_path == null">
      </div>
      <div class="info">
          <h1>Titolo: {{film.title}}</h1>
          <h3>Titolo Originale: {{film.original_title}}</h3>
          <LangFlag :iso="film.original_language" v-if="(film.original_language !== undefined)"></LangFlag>
          <div class="stars">
              <h5>Voto: </h5><i class="fa-solid fa-star" v-for="i in Math.ceil(film.vote_average / 2)" :key="i"></i>
          </div>
          <br>
          <h5 v-if="(film.overview !== '')">Overview: {{film.overview}}</h5>
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
    border: 1px solid rgb(150, 150, 150);
    padding: 5px;
    position: relative;
    :hover{
                .info{
                    display: block;
                    position: absolute;
                    top: 0;
                    left: 0;
                    padding: 10px;
                    overflow: auto;
                }
            }
    .pic{
        img{
            width: 100%;
            aspect-ratio: 9/16;
        }
    }
    .info{
        background-color: rgba(0, 0, 0, 0.7);
        height: 100%;
        width: 100%;
        display: none;
        color: white;
        .stars{
            display: flex;
            flex-flow: row nowrap;
            gap: 2px;
            i{
                color: rgb(213, 193, 12);
            }
        }
    }
    h1{
        font-size: 14px;
    }
    h3{
        font-size: 12px
    }
}
</style>