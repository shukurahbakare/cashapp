<script>
import IconSupport from "@/components/icons/IconSupport.vue";
import IconEasy from "@/components/icons/IconEasy.vue";
import IconRocket from "@/components/icons/IconRocket.vue";
import IconShield from "@/components/icons/IconSheild.vue";

export default {
  components: {
    IconSupport,
    IconEasy,
    IconRocket,
    IconShield
  },
  data() {
    return {
      top_countries_arr: [
        {
          icon: "IconEasy",
          name: "Cameroon",
        },
        {
          icon: "IconSupport",
          name: "Côte d'Ivoire",
        },
        {
          icon: "IconRocket",
          name: "Ghana",
        },
        {
          icon: "IconShield",
          name: "Kenia",
        }
      ]
    };
  }
};
</script>

<template>
  <section class="top_countries">
    <div class="top_countries_container">
      <h1>
        Top Countries
      </h1>
      <div class="top_countries_container_content">
        <div class="top_countries_container_content_card" v-for="feature in top_countries_arr" :key="feature.name">
          <div class="top_countries_container_content_card_icon">
            <component :is="feature.icon" />
          </div>
          <div class="top_countries_container_content_card_title">
            <p>{{ feature.name }}</p>
          </div>
          
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
@use "../styles/index.scss" as *;

.top_countries {
  padding: 3rem 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-bottom: 4rem;

  &_container {
    width: 100%;
    max-width: $max-w-6xl;

    &_content {
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: 1.5rem;
      overflow: hidden;

      &_card {
        opacity: 0; // Initially hidden
        transform: translateY(20px); // Initially positioned lower
        animation: fadeInUp 0.6s ease forwards; // Animation properties

        p {
          color: #5F5F65;
          font-size: 16px;
          font-weight: 400;
          line-height: 24px;
        }
      }
    }
  }

  @keyframes fadeInUp {
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  // Add a loop to generate the delay for each card
  @for $i from 1 through 12 {
    .top_countries_container_content_card:nth-of-type(#{$i}) {
      animation-delay: #{0.2 * $i}s;
    }
  }
}
</style>
