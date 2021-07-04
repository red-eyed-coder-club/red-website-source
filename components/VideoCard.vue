<template>
  <NuxtLink :to="`/courses/${courseInfo.slug}`" class="card col-4">
    <div class="card-body d-flex flex-column text-left">
      <h2 class="card-text card-title my-4">
        {{ courseInfo.title }}
        <span v-if="!courseInfo.accessible" class="badge text-dark bg-warning">
          In progress
        </span>
      </h2>

      <p class="card-meta">
        <span class="icon-clock2"></span>
        <span class="duration">{{ courseInfo.duration }}</span> |
        <span class="videos">{{ courseInfo.videos }} {{ courseInfo.videos > 1 ? 'videos' : 'video'}}</span>
      </p>
      <p class="card-description mb-5">{{ courseInfo.description }}</p>
    </div>
    <div class="card-footer text-muted">
      {{ courseInfo.level }}
    </div>
  </NuxtLink>
</template>

<script>
  export default {
    props: [
      'courseInfo'
    ]
  }
</script>

<style scoped>
.col-4 {
  padding: 0;
  margin: 2rem;
}

h2 > span {
  font-size: 0.8rem;
  margin-left: 0.7rem;
}

.card {
  text-decoration: none;
  color: #333;
  /* min-width: 20rem; */
  max-width: 25rem;
  background: #f9fbff;
  border-radius: 10px !important;
}

.card-title {
  font-size: 1.625rem;
  font-weight: 600;
  color: #38416f;
  min-height: 4rem;
}

.card-meta {
  font-size: 1.1rem;
}

.card-description {
  font-size: 1.15rem;
}

span.duration {
  margin-left: 0.3rem;
  margin-right: 0.7rem;
}

span.videos {
  margin-left: 0.7rem;
}

.card:hover {
  box-shadow: 0 .44rem .85rem rgba(0, 0, 0, .07);
}
</style>
