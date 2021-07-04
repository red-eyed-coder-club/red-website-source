<template>
    <footer>
      <div class="footer-wrapper row justify-content-center">

        <div class="col-6 text-center mt-5 mb-4">

          <div class="footer-icons row justify-content-center mb-4">
            <div class="icon i-patreon">
              <a href="https://www.patreon.com/red_eyed_coder_club"><span class="icon-patreon"></span></a>
            </div>
            <div class="icon i-youtube">
              <a href="https://www.youtube.com/channel/UCh_LSaTv2GeZ3woJNTGihew"><span class="icon-youtube"></span></a>
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
    margin-top: 6rem;
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

  .i-patreon a {
    color: #ff424d;
    text-decoration: none;
  }

  .i-youtube a {
    color: red;
    text-decoration: none;
  }
</style>
