<template>

    <div class="col-12 mx-auto text-center">
      <div class="hero">
        <h1 class="hero-header">Courses</h1>
        <h4 class="subheader">The index page of all my courses</h4>
      </div>

      <div class="card-deck row justify-content-center">

        <VideoCard
          v-for="(course, index) in coursesTier.items"
          :key="index"
          :courseInfo="course"
        />
        
      </div>
    </div>

</template>

<script>
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
