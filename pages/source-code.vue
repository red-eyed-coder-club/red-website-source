<template>
  <div class="col-lg-11 col-md-12 col-sm-12 mx-auto text-center">
    <div class="hero">
      <h1 class="hero-header">Source Code</h1>

      <h4 class="subheader mt-3 mb-5">of all projects on the <a href="https://www.youtube.com/channel/UCh_LSaTv2GeZ3woJNTGihew">Youtube channel</a></h4>

      <PatreonButton
        :textButton="`Get Access`"
      />
    </div>

    <section class="text-left mb-5" id="index">
      <h2 class="mb-5">Index of Source Code Tier</h2>

      <div v-for="(sourceCode, index) in sourceCodeTier.items" :key="index" class="row justify-content-between align-items-center video-link">

        <div class="source-title">
          <a :href="sourceCode.code" target="_blank">{{ sourceCode.title }}</a>
        </div>

        <div class="buttons-wrapper row">
          <div class="button-wrapper mr-4">
            <a class="btn button youtube-button" :href="sourceCode.video" target="_blank">
              <span class="icon-youtube"></span>
              Watch Video
            </a>
          </div>

          <div class="button-wrapper">
            <a class="btn button source-button" :href="sourceCode.code" target="_blank">
              <span class="icon-file-download"></span>
              Source Code
            </a>
          </div>
        </div>

      </div>
    </section>

  </div>
</template>

<script>
  import { mapState } from 'vuex'

  export default {
    computed: mapState({
      sourceCodeTier: state => state.tiers.find(tier => tier.title === 'Source Code')
    })
  }
</script>

<style scoped>
  .video-link {
    border-bottom: 1px solid rgba(0, 0, 0, 0.05);
    text-decoration: none;
    color: #333;
    padding: 0.5rem 0;
    font-size: 1.2rem;
    margin-right: 0;
    margin-left: 0;
  }
  .video-link:hover {
    background: #f9fbff;
  }

  .video-link-icon {
    margin-right: 0.5rem;
    color: #dd2e44;
  }

  .button {
    color: #333;
    border: 1px solid #dddddd;
  }

  .youtube-button:hover {
    color: #fff;
    border: 1px solid red;
    background: red;
  }

  .source-button:hover {
    color: #fff;
    border: 1px solid #444;
    background: #555;
  }

  @media(max-width: 1000px){
    .video-link {
      display: flex;
      flex-direction: column;
      margin: 2rem;
      padding: 1rem 0 3rem 0;

      border-radius: 5px;
      border: 1px solid #ddd;
      box-shadow: 3px 5px 5px rgba(125, 125, 125, 0.3);
    }

    .video-link:hover {
      background: none;
    }

    .source-title {
      margin-top: 2rem;
      text-align: center;
    }

    .buttons-wrapper {
      margin: 2rem 0 0 0;
    }
  }

  @media(max-width: 530px) {
    h2 {
      text-align: center;
    }
  }

  @media(max-width: 375px) {

    .video-link {
      padding-bottom: 1rem;
    }

    .buttons-wrapper {
      justify-content: center;
      flex-direction: column;
    }
    .button-wrapper  {
      margin-right: 0 !important;
      margin-bottom: 2rem;
    }
  }

</style>
