<template>
  <div id="app">
    <MainHeader></MainHeader>
    <MainMain></MainMain>
  </div>
</template>

<script>
import MainHeader from './components/Organism/MainHeader.vue';
import MainMain from './components/Organism/MainMain.vue';

export default {
  name: 'App',
  components: {
    MainHeader,
    MainMain
}
}
</script>

<style lang="scss">
@import './assets/style/global-parts/reset';
body{
  background-color: rgb(25, 25, 25);
}
</style>
