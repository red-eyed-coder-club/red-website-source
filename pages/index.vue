<template>
  <div class="container">
    <Hero />

    <div class="card-deck row justify-content-center">
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
