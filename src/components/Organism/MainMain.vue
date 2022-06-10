<template>
    <main>
        <FilmsContainer></FilmsContainer>
        <SeriesContainer></SeriesContainer>
    </main>
</template>

<script>
import  FilmsContainer from '../Molecules/FilmsContainer.vue'
import  SeriesContainer from '../Molecules/SeriesContainer.vue'

export default {
name: 'MainMain',
components: { FilmsContainer, SeriesContainer }
}
</script>

<style>

</style>