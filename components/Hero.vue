<template>
  <div class="mx-auto text-center hero">
    <h1 class="hero-header">Patreon Index</h1>
    <h4 class="hero-subheader">Patreon has extremely bad UX, so I made this Index page.</h4>

    <p class="hero-description mt-5">
      My Patrons can have access to <NuxtLink to="/source-code"><strong>Source Code</strong></NuxtLink> of all my projects,<br>
      and to all available content via the <NuxtLink to="/courses"><strong>Courses</strong></NuxtLink> tiers
    </p>
  </div>
</template>

<script>
  export default {

  }
</script>

<style scoped>
  .hero {
    padding: 7rem 0 4rem 0;
  }
  .hero-header {
    font-weight: 700;
    font-size: 3rem;
  }
  .hero-subheader {
    font-size: 1.6rem;
  }
  .hero-description {
    font-size: 1.3rem;
  }
</style>
