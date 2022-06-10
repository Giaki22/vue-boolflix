<template>
  <main>
      <div class="pic">
      </div>
      <div class="info">
          <h1>{{serie.name}}</h1>
          <h3>{{serie.original_name}}</h3>
          <LangFlag :iso="serie.original_language" v-if="(serie.original_language !== undefined)"></LangFlag>
          <h5>{{serie.vote_average / 2}}</h5>
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

<style>

</style>