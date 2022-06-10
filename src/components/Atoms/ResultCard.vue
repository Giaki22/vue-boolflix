<template>
  <main>
      <div class="pic">
      </div>
      <div class="info">
          <h1>{{film.title}}</h1>
          <h3>{{film.original_title}}</h3>
          <h5>{{film.original_language}}</h5>
          <h5>{{film.vote_average / 2}}</h5>
      </div>
  </main>
</template>

<script>
export default {
name: 'ResultCard',
props: {
    film: Object
}
}
</script>

<style>

</style>