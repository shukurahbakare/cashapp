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
      features_arr: [
        {
          icon: "IconEasy",
          name: "Easy to Sign Up",
          desc: "Link your debit card, verify your identity and be sending in minutes."
        },
        {
          icon: "IconSupport",
          name: "24/7 Support",
          desc: "We are available to chat 24/7 if you need any help."
        },
        {
          icon: "IconRocket",
          name: "Fast & Convenient",
          desc: "Skip the line and send money from your phone to your loved ones in seconds."
        },
        {
          icon: "IconShield",
          name: "Trusted and Legitimate",
          desc: "Trusted by over 1 million users, BNB Cash App is operated by BNB Transfer."
        }
      ]
    };
  }
};
</script>

<template>
  <section class="features">
    <div class="features_container">
      <div class="features_container_content">
        <div class="features_container_content_card" v-for="feature in features_arr" :key="feature.name">
          <div class="features_container_content_card_icon">
            <component :is="feature.icon" />
          </div>
          <div class="features_container_content_card_title">
            <h1>{{ feature.name }}</h1>
          </div>
          <div class="features_container_content_card_desc">
            <p>{{ feature.desc }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
@use "../styles/index.scss" as *;

.features {
  padding: 3rem 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-bottom: 4rem;

  &_container {
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
    .features_container_content_card:nth-of-type(#{$i}) {
      animation-delay: #{0.2 * $i}s;
    }
  }
}
</style>
