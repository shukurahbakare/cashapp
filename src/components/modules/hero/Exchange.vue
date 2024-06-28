<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <aside class="exchange-section">
    <header class="exchange-section_header">
      <span>Exchange Rate</span>
      <p>1 CAD ≈ 1,090.21 NGN</p>
    </header>
    <div class="exchange-section_details">
      <div class="exchange-section_details_content">
        <h1>
          Calculate Rates
        </h1>
        <div class="exchange_cards">
          <div>
            <span>You Send</span>
            <p>$ 0</p>
          </div>
          <div>
            <span>You Send</span>
            <p>₦ 0</p>
          </div>
<p class="exchange-section_footer">Exchange Rate: 1 GBP = 158.48 Ksh <br />
        Transfer fees: 0.00 GBP</p>
        </div>

      </div>

      
    </div>

  </aside>


</template>

<style lang="scss" scoped>
@use "../../../styles/index.scss" as *;

p, h1, span {
  margin: 0;
}

.exchange-section {
  width: 100%;
  display: flex;
  flex-direction: column;
  border-radius: 1.5rem;
  background-color: #2A2A2A;
  overflow: hidden;

  &_details {
    padding: 0.5rem 1.5rem 1.5rem 1.5rem ;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 100%;
    

    &_content{
      display: grid;
      gap: 1rem;

      h1 {
        color: white;
        font-size: 20px;
        font-weight: 700;
      }
    }

    .exchange_cards {
      display: grid;
      grid-template-columns: repeat(1, minmax(0, 1fr));
      gap: 1.5rem;

      div {
        background-color: white;
        padding: 0.5rem 1rem;
        border-radius: 1rem;

        span {
          font-size: 12px;
          opacity: 0.5;
          margin-bottom: -0.5rem;
          display: block;
        }  

        p {
          color: #5F5F65;
          font-size: 28px;
          font-weight: 500;
        }
      }
    }
  }

  &_header {
    background-color: rgba(255, 255, 255, 0.10);
    padding: 1rem;
    color: #fff;
    text-align: center;

    p {
      text-shadow: 1px 1px 0px rgba(0, 0, 0, 0.25);
      font-size: 20px;
      font-weight: 600;
    }

  }

  &_footer {
    width: 100%;
    border-radius: 0.5rem;
    padding: 1rem 0;
    background-color: #ffffff1a;
    color: #ffffff99;
    line-height: 1.25rem;
    text-align: center;
  }
}
</style>