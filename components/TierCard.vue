<template>
  <NuxtLink :to="cardData.url" class="card text-center">
    <div class="card-header">
      <h3 class="card-title">{{ cardData.title }}</h3>
    </div>
    <div class="card-body d-flex flex-column">
      <p class="card-text items my-4">
        {{ cardData.items.length }} {{ cardData.items.length > 1 ? 'items' : 'item'}}
      </p>
      <p class="includes" v-for="include in cardData.includes">{{ include }}</p>
      <NuxtLink :to="cardData.url" class="btn btn-outline-primary mt-auto mb-3 align-self-center">More details</NuxtLink>
    </div>
    <div class="card-footer text-muted">
      $ {{ cardData.price }} per month
    </div>
  </NuxtLink>
</template>

<script>
  export default {
    props: [
      'cardData'
    ]
  }
</script>

<style scoped>
  /* .col-4 {
    padding: 0;
  } */
  .card {
    text-decoration: none;
    color: #333;
    min-width: 21rem;
    max-width: 22rem;
  }

  .card .items {
    font-size: 2.5rem;
    font-weight: 800;
  }

  .card:hover {
    box-shadow: 0 .44rem .85rem rgba(0, 0, 0, .07);
  }

  @media(max-width: 980px) {
    .card {
      margin-bottom: 4rem;
    }
  }
</style>
