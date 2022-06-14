<template>
  <main>
    <div class="logo">
      <BasicLogo></BasicLogo>
    </div>
    <div class="search">
      <SearchBar></SearchBar>
      <SearchButton></SearchButton>
    </div>
  </main>
</template>

<script>
import SearchBar from '../Atoms/SearchBar.vue'
import SearchButton from '../Atoms/SearchButton.vue'
import BasicLogo from '../Atoms/basicLogo.vue'

export default {
  components: { SearchBar, SearchButton, BasicLogo },
name: 'MainHeader'
}
</script>

<style scoped lang="scss">
main{
    display: flex;
    flex-flow: row nowrap;
    justify-content: space-around;
    background-color: black;
    align-items: center;
    .logo{
      width: 50px;
    }
    .search{
      display: flex;
      flex-flow: row nowrap;
      height: 30px;
    }
}
</style>