<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <aside  class="qr-section">
    <div class="qr-section_image">
      <!-- <img src="../../assets/hero_woman.png" alt="Our happy user"> -->
    </div>
    <div class="qr-section_details">
      <!-- <img src="../../assets/qr_code.png" alt=""> -->
      <p>Exchange Rate: 1 GBP = 158.48 Ksh <br/>
        Transfer fees: 0.00 GBP</p>
    </div>

  </aside>


</template>

<style lang="scss" scoped>
@use "../../../styles/index.scss" as *;

.qr-section {
  width: 100%;
  display: flex;
  flex-direction: column;
  border-radius: 1rem;
  background-color: #2A2A2A;
  overflow: hidden;

  &_details {
    padding: 1rem;
    display: flex;
    align-items: center;
    gap: 1rem;

    img {
      width: 7rem;
    }

    p {
      line-height: 1.25rem;
      text-align: center;
    }
  }

  &_image {
    overflow: hidden;
    img {
      width: 100%;
    }
  }
}


</style>