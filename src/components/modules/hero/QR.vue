<script setup>
</script>

<template>
  <aside  class="qr-section">
    <div class="qr-section_image">
      <img src="../../assets/hero_woman.png" alt="Our happy user">
    </div>
    <div class="qr-section_details">
      <img src="../../assets/qr_code.png" alt="">
      <p>Scan to download app. <br />
        Available on Appstore and Playstore.</p>
    </div>

  </aside>


</template>

<style lang="scss" scoped>
@use "../../../styles/index.scss" as *;

.qr-section {
  width: 100%;
  display: flex;
  flex-direction: column;
  border-radius: 1.5rem;
  background-color: white;
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