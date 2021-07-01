<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <div class="container">

        <NuxtLink class="navbar-brand" to="/">
          <img src="@/assets/images/logo_36.png" class="mr-2">
          Red Eyed Coder Club
        </NuxtLink>

        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0 ml-auto">
            <li class="nav-item">
              <NuxtLink class="nav-link active" aria-current="page" to="/courses">Courses</NuxtLink>
            </li>
            <li class="nav-item">
              <NuxtLink class="nav-link" to="/source-code">Source Code</NuxtLink>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
  export default {

  }
</script>

<style scoped>
  
</style>
