<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <div class="container">
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
    </div>

  </header>

  <RouterView />
</template>

<style lang="scss" scoped>
@use "./styles/index.scss" as *;

header {
  display: flex;
  justify-content: center;
  align-items: center;

  .container {
    max-width: $max-w-6xl;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  nav {
    width: 100%;
    font-size: 12px;
    text-align: center;
    display: flex;
    gap: 2rem;
    font-size: 1.2rem;

    @include custom-media-query("mobile", $max-w-lg) {
      display: none;
    }

    a {
      text-decoration: none;
      color: black;

    }

    a.router-link-exact-active {
      color: $primary;
    }
  }

  button {
    padding: 0.5rem 1.5rem;
    border-radius: 3rem;
    background-color: $primary;
    border: 2px solid $primary;
    font-size: 20px;
    font-weight: 500;
    line-height: 30px;

    a {
      color: #fff;
      text-decoration: none;
    }
  }
}
</style>
