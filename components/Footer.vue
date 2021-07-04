<template>
  <footer>
    <div class="footer-wrapper row justify-content-center">
      <div class="col-6 text-center mt-5 mb-4">
        <div class="footer-icons row justify-content-center mb-4">
          <div class="icon icon-patreon">
            <a href="https://www.patreon.com/red_eyed_coder_club"><font-awesome-icon :icon="['fab','patreon']" /></a>
          </div>
          <div class="icon icon-youtube">
            <a href="https://www.youtube.com/channel/UCh_LSaTv2GeZ3woJNTGihew"><font-awesome-icon :icon="['fab','youtube']" /></a>
          </div>
        </div>
        <p>
          &copy; 2021-present, <a href="https://www.youtube.com/channel/UCh_LSaTv2GeZ3woJNTGihew" class="youtube-link">Red Eyed Coder Club</a>
          <br>
          &copy; 2021-present, Oleg Molchanov
        </p>
      </div>

    </div>
  </footer>
</template>

<script>
  export default {

  }
</script>

<style scoped>
  footer {
    background: #333;
    box-shadow: inset 0px 10px 30px #000;
    color: white;
    overflow: hidden;
  }

  .youtube-link {
    color: #729ecf;
  }

  .youtube-link:hover {
    color: #729ecf;
  }

  .icon {
    padding: 1rem 1.3rem;
    font-size: 2rem;
  }

  .icon-patreon a {
    color: #ff4240;
  }

  .icon-youtube a {
    color: red;
  }
</style>
