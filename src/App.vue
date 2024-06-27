<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <!-- <HelloWorld msg="You did it!" /> -->

      <nav>
        <RouterLink to="/">For Businesses</RouterLink>
        <RouterLink to="/partners">Payout Partners</RouterLink>
        <RouterLink to="/about">About Us</RouterLink>
        <RouterLink to="/careers">Careers</RouterLink>
        <RouterLink to="/help">Help</RouterLink>
      </nav>
    </div>

    <button>
      <RouterLink to="/login">Download App</RouterLink>
    </button>
  </header>

  <RouterView />
</template>

<style lang="scss" scoped>
@use "./styles/index.scss" as *;

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  border: 2px solid red;

  nav {
    width: 100%;
    font-size: 12px;
    text-align: center;
    display: flex;
    gap: 1rem;
    font-size: 1.2rem;

    a.router-link-exact-active {
      color: $primary;
    }
  }

  button {
    background-color: $primary;
    border: 2px solid $primary;
  }
}
</style>
