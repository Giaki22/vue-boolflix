<template>
  <main>
      <input type="text" v-model="data.searchText" placeholder="Search Film or Tv Serie...">
  </main>
</template>

<script>
import data from '../../assets/shared/data.js'

export default {
name: 'SearchBar',
data() {
    return {
        data
    }
}
}
</script>

<style scoped>
input{
    line-height: 26px;
}
</style>