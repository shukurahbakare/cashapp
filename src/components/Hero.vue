<script setup>


import QR from './modules/hero/QR.vue'
import Exchange from './modules/hero/Exchange.vue'
</script>

<template>

  <section class="hero">
    <div class="hero_container">
      <h1>Sending Made Easy</h1>
    </div>

    <section class="hero_modules">
      <QR />
      <Exchange />
    </section>

  </section>

</template>

<style lang="scss" scoped>
@use "../styles/index.scss" as *;

.hero {
  margin-top: -1rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 3rem;
  background-color: $primary;
  background: $primary-gradient;
  padding-bottom: 2rem;


  &_container {
    max-width: $max-w-5xl;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;

    h1 {
      position: relative;
      font-size: clamp(1rem, -0.3323rem + 5.988vw, 3.5rem);
      z-index: 1;
      background-color: transparent;

      &::before {
        content: "";
        width: 100%;
        height: 20px;
        position: absolute;
        top: 3.75rem;
        left: 0;
        background-image: url("./icons/Subtract.png");
        background-repeat: no-repeat;
        background-size: contain;
        z-index: -1;
      }
    }

  }

  &_modules {
    max-width: $max-w-5xl;
    width: 100%;
    display: grid;
    grid-template-columns: repeat(5, minmax(0, 1fr));
    gap: 2rem;

    @include custom-media-query("mobile", $max-w-md) {
      grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    aside {

      &:first-child {
        grid-column: span 3 / span 3;
        @include custom-media-query("mobile", $max-w-md) {
          grid-column: span 1 / span 1;
        }
      }

      &:last-child {
        grid-column: span 2 / span 2;
        @include custom-media-query("mobile", $max-w-md) {
          grid-column: span 1 / span 1;
        }
      }
    }
  }
}
</style>