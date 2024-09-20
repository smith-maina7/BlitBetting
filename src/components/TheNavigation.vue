<script setup>
import { ref } from 'vue'
import leaguesData from '../data/linksData.json' // Import your JSON data

const dropdown = ref(false)
let hideTimeout = null

const toggleDropdown = (show) => {
  if (show) {
    clearTimeout(hideTimeout)
    dropdown.value = true
  } else {
    hideTimeout = setTimeout(() => {
      dropdown.value = false
    }, 1000)
  }
}
</script>

<template>
  <nav>
    <!-- Logo with link to home -->
    <div class="navbar-logo">
      <router-link to="/">
        <img src="../assets/Images/Others/bettingblitz2.png" alt="logo" class="navbar-logo-img" />
      </router-link>
    </div>

    <!-- Navigation Links -->
    <div class="navbar-links">
      <!-- Home link -->
      <router-link to="/" class="navbar-link">Home</router-link>

      <!-- Football dropdown -->
      <div
        class="navbar-link"
        @mouseover="toggleDropdown(true)"
        @mouseleave="toggleDropdown(false)"
      >
        Football
        <ul v-if="dropdown">
          <li v-for="league in leaguesData.leagues" :key="league.id">
            <router-link :to="{ name: 'football', params: { id: league.id } }" class="navbar-link">
              <img :src="`../assets/Images/Countrys/${league.image}`" :alt="league.country" />
              {{ league.country }}
            </router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>
/* Your styling remains unchanged */
</style>
