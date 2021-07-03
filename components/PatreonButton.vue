<template>
    <div class="get-access-button">
      <a href="https://www.patreon.com/red_eyed_coder_club" class="btn btn-danger patreon-button">{{ textButton }}</a>
    </div>
</template>

<script>
  export default {
    props: [
      'textButton'
    ]
  }
</script>

<style scoped>
  .patreon-button {
    padding: 0.8rem 3.8rem;
    border-radius: 10px;
    font-size: 1.3rem;
    font-weight: 700;
  }
</style>
