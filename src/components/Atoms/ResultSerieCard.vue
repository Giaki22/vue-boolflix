<template>
  <main>
      <div class="pic">
        <img :src="`https://image.tmdb.org/t/p/w780${serie.poster_path}`" v-if="serie.poster_path !== null">
        <img :src="`https://cdn1.iconfinder.com/data/icons/leto-files/64/leto_files-58-512.png`" v-if="serie.poster_path == null">
      </div>
      <div class="info">
          <h1>{{serie.name}}</h1>
          <h3>{{serie.original_name}}</h3>
          <LangFlag :iso="serie.original_language" v-if="(serie.original_language !== undefined)"></LangFlag>
          <div class="stars">
              <h5>{{Math.ceil(serie.vote_average / 2)}}</h5>
          </div>
      </div>
  </main>
</template>

<script>
import LangFlag from 'vue-lang-code-flags';

export default {
    name: "ResultSerieCard",
    props: {
        serie: Object
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
}
</style>