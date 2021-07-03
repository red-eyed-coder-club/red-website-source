<template>
  <div class="col-9 mx-auto text-center">
    <div class="hero">
      <h1 class="hero-header">Source Code</h1>

      <h4 class="subheader mt-3 mb-5">of all projects on the <a href="https://www.youtube.com/channel/UCh_LSaTv2GeZ3woJNTGihew">Youtube channel</a></h4>

      <PatreonButton
        :textButton="`Get Access`"
      />
    </div>

    <section class="course-index text-left mb-5" id="index">
      <h2 class="mb-5">Index of Source Code Tier</h2>

        <div v-for="(sourceCode, index) in sourceCodeTier.items" :key="index">

          <div class="row justify-content-between align-items-center video-link">

            <div class="row justify-content-start">
              <span class="video-link-icon">
                <font-awesome-icon :icon="['fas','file-download']" />
              </span>
              <a :href="sourceCode.code">{{ sourceCode.title }}</a>
            </div>

            <div class="">
                <a class="btn youtube-button" :href="sourceCode.video">
                  <span>
                    <font-awesome-icon :icon="['fab','youtube']" />
                  </span>
                  Watch Video
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
  }
  .video-link:hover {
    background: #f9fbff;
  }

  .video-link-icon {
    margin-right: 0.5rem;
    color: #dd2e44;
  }

  .youtube-button {
    color: #333;
    border: 1px solid #dddddd;
  }

  .youtube-button:hover {
    color: #fff;
    border: 1px solid red;
    background: red;
  }
</style>
