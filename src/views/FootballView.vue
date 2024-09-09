<script setup>
import { computed } from 'vue'
import { useRoute } from 'vue-router'
import linksdata from '../data/linksData.json'

// Get the route parameters
const route = useRoute()
// Extract the footballId from the route params and convert it to an integer
const footballId = parseInt(route.params.id)
console.log(footballId)
// Access the leagues array and find the matching league based on the id
const leagueDestination = computed(() => linksdata.leagues.find((link) => link.id === footballId))
console.log(leagueDestination.value)
</script>

<template>
  <template> </template>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
