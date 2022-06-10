<template>
  <main>
      <SearchBar></SearchBar>
      <SearchButton></SearchButton>
  </main>
</template>

<script>
import SearchBar from '../Atoms/SearchBar.vue'
import SearchButton from '../Atoms/SearchButton.vue'

export default {
  components: { SearchBar, SearchButton },
name: 'MainHeader'
}
</script>

<style scoped>
main{
    display: flex;
    flex-flow: row nowrap;
}
</style>