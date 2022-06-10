<template>
  <main>
      <div class="pic">
      </div>
      <div class="info">
          <h1>{{film.title}}</h1>
          <h3>{{film.original_title}}</h3>
          <LangFlag :iso="film.original_language" v-if="(film.original_language !== undefined)"></LangFlag>
          <h5>{{film.vote_average / 2}}</h5>
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

<style>

</style>