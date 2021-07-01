<template>
  <div class="container">
    <Hero />

    <div class="cards-wrapper d-flex justify-content-around">
      <TierCard
        v-for="(tierCard, index) in tiers"
        :key="index"
        :cardData="tierCard"
      />
    </div>

  </div>
</template>

<script>
  import { mapState } from 'vuex'

  export default {
    computed: mapState({
      tiers: state => state.tiers
    })
  }
</script>
