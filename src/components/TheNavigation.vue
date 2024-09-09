<script setup>
import { ref } from 'vue'
// import links from '@/components/TheLinks.vue' // uncomment this line once you set up dynamic routing

const dropdown = ref(false)
let hideTimeout = null

const toggleDropdown = (show) => {
  if (show) {
    clearTimeout(hideTimeout)
    dropdown.value = true
  } else {
    hideTimeout = setTimeout(() => {
      dropdown.value = false
    }, 1000) // Adjust the delay as needed
  }
}
</script>
```

<template>
  <nav>
    <div class="navbar-logo">
      <router-link to="/"
        ><img
          src="../assets/Images/Others/bettingblitz2.png"
          alt="image of logo"
          class="navbar-logo-img"
      /></router-link>
    </div>

    <div class="navbar-links">
      <router-link to="/" class="navbar-link">Home</router-link>
      <div
        class="navbar-link"
        @mouseover="toggleDropdown(true)"
        @mouseleave="toggleDropdown(false)"
      >
        Football
        <ul v-if="dropdown">
          <li>
            <router-link to="/about" class="navbar-link">
              <img src="../assets/Images/Countrys/England flag.png" alt="Premier league Image" />
              England
            </router-link>
          </li>
          <li>
            <router-link to="/" class="navbar-link">
              <img src="../assets/Images/Countrys/Spain flag.png" alt="La Liga Image" />
              Spain
            </router-link>
          </li>
          <li>
            <router-link to="/" class="navbar-link"
              ><img
                src="../assets/Images/Countrys/France flag.jpg"
                alt="League 1 Image"
              />France</router-link
            >
          </li>
          <li>
            <router-link to="/" class="navbar-link"
              ><img
                src="../assets/Images/Countrys/Italy flag.png"
                alt="Serie A Image"
              />Italy</router-link
            >
          </li>
          <li>
            <router-link to="/" class="navbar-link"
              ><img
                src="../assets/Images/Countrys/Germany flag.png"
                alt="Bundesliga Image"
              />Germany</router-link
            >
          </li>
          <li>
            <router-link to="/" class="navbar-link"
              ><img
                src="../assets/Images/Countrys/Netherlands flag.png"
                alt="Eredivise Image"
              />Netherlands</router-link
            >
          </li>
          <!-- <links /> -->
          <!-- Import TheLinks component and use it here -->
        </ul>
      </div>
      <router-link to="/" class="navbar-link">Basketball</router-link>
      <router-link to="/" class="navbar-link">Tennis</router-link>
      <router-link to="/" class="navbar-link">Formula1</router-link>
    </div>

    <div class="navbar-auth">
      <router-link to="/" class="navbar-login">Login</router-link>
      <router-link to="/" class="navbar-join">Join</router-link>
    </div>
  </nav>
</template>
