<script setup>
import { computed } from 'vue'
import { useRoute } from 'vue-router'
import linksdata from '../data/linksData.json'

// Get the route parameters
const route = useRoute()
const footballId = parseInt(route.params.id)

// Compute the league based on the ID
const leagueDestination = computed(() => linksdata.leagues.find((link) => link.id === footballId))
console.log(leagueDestination.value.country)
</script>

<template>
  <div v-if="leagueDestination">
    <h2>{{ leagueDestination.country }} League</h2>
    <h2>{{ leagueDestination.country }}: League</h2>
    <img
      :src="`../assets/Images/Countrys/${leagueDestination.image}`"
      :alt="leagueDestination.country"
    />
  </div>
  <div v-else>
    <h2>League not found</h2>
  </div>
</template>

<style scoped>
img {
  max-width: 100px;
  height: auto;
}
</style>
