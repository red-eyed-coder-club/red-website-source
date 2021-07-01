<template>
  <div class="mx-auto text-center hero">
    <h1 class="hero-header">Courses</h1>
    <h4 class="subheader">The index page of all my courses</h4>
  </div>
</template>

<script>
  import { mapState } from 'vuex'

  export default {
    computed: {
      coursesTier(){
        return this.$store.getters.getCoursesTier();
      }
    }
  }
</script>

<style scoped>

</style>
