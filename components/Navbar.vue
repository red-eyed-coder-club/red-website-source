<template>
  <!-- <div> -->
    <b-navbar toggleable="lg" type="dark" variant="dark">
      <div class="container">

        <NuxtLink class="navbar-brand" to="/">
          <img src="@/assets/images/logo_36.png" class="mr-2">
          Red Eyed Coder Club
        </NuxtLink>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" class="nav-right-links" is-nav>
          <b-navbar-nav class="ml-auto">
            <NuxtLink class="nav-link active" to="/courses">Courses</NuxtLink>
            <NuxtLink class="nav-link" to="/source-code">Source Code</NuxtLink>
          </b-navbar-nav>
        </b-collapse>
      </div>
    </b-navbar>
  </div>
</template>

<script>
  export default {

  }
</script>

<style scoped>
  .nav-right-links {
    font-size: 1.2rem;
  }
</style>
