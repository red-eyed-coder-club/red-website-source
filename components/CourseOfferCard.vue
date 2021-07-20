<template>
  <a href="https://www.patreon.com/red_eyed_coder_club" class="card col-6">
    <div class="card-body d-flex flex-column text-center">
      <h2 class="card-text card-title my-3">
        Courses Tier
      </h2>
      <h3 class="card-subtitle mb-3">
        Access to this and all other current & future courses and source code!
      </h3>

      <div class="price mt-3">$10/month</div>
      <p class="price-details">+ VAT added on checkout page</p>

      <p class="my-4">Cancel anytime!</p>

      <p class="card-description mb-5">This is a recurring payment, charged automatically on a mothly basis. You can cancel anytime from inside your user profile to avoid being charged again once your billing cycle ends.</p>

      <PatreonButton
        :textButton="`Subscribe`"
      />

    </div>
  </a>
</template>

<script>
  export default {
  }
</script>

<style scoped>
  .col-5 {
    padding: 0;
    margin: 2rem;
  }

  .card {
    text-decoration: none;
    color: #333;
    min-width: 20rem;
    max-width: 30rem;
    background: #f9fbff;
    border-radius: 10px !important;
  }

  .card-title {
    font-size: 2rem;
    font-weight: 700;
    color: #38416f;
    min-height: 4rem;
  }

  .card-subtitle {
    font-size: 1.2rem;
    font-weight: bold;
  }

  .price {
    font-size: 3.5rem;
    font-weight: 700;
  }

  .price-details {
    font-size: 1rem;
  }

  .card-description {
    font-size: 1.15rem;
  }

  .card-description {
    font-size: 1rem;
  }

  .card:hover {
    box-shadow: 0 .44rem .85rem rgba(0, 0, 0, .07);
  }
</style>
