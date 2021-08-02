<template>

    <div class="main-content col-lg-9 col-md-11 col-sm-12 mx-auto text-center">
      <div class="hero">
        <h1 class="hero-header">Practical Python: <br> Logging</h1>

        <h2 class="subheader my-4">How to build a monitoring system for your Python project</h2>

        <div class="hero-meta my-4 mb-5">
          {{ courseInfo.duration }} | {{ courseInfo.videos }} videos
        </div>

        <PatreonButton
          :textButton="`Get Access`"
        />
      </div>

      <Sidebar />

      <section class="about text-left justify-content-center" id="about">
        <div class="about-content">
          <h2>What is this course about?</h2>

          <p>
            This course is about Python Logging module, one of the most misunderstood and unclear module in Python, and about its usage in your Python projects.<br>
          </p>
          <p>
            <strong>
              Without the Logging module it's barely possible to get even a bit of information what's happened with your Python project deployed on a server
            </strong>.
          </p>

          <p>When your user pointing you out about some bugs with your project it will be almost impossible to fix it, because you don't know what the User did, what data was passed in to your project, and what's happened.</p>

          <p>You have no access to Python traceback, no prints, and no data.</p>

          <p>But! You need to collect the debuging information.</p>

          <p>How can you get it?</p>

          <p>
            Fortunately the Logging module allows us to build a monitoring system, that will collect debuging data, message you about errors by email, SMS, Telegram Bot and so on.
          </p>
        </div>
      </section>

      <section class="course-traits row justify-content-center">
        <div class="col-md-5">
          <h2 class="mb-3">1.5</h2>
          <h3>hours</h3>
        </div>
        <div class="col-md-5">
          <h2 class="mb-3">{{ courseInfo.videos }}</h2>
          <h3>videos</h3>
        </div>
      </section>

      <section class="course-index text-left" id="index">
        <h2>Index of Course</h2>

        <div>
          <div v-for="(video, index) in courseInfo.map" :key="index">
            <a :href="video.patreon_url" class="row justify-content-between video-link">

              <div>
                <span class="video-link-icon">
                  <span class="icon-youtube"></span>
                </span>
                {{ video.title }}
              </div>

              <div>
                {{ video.duration }}
              </div>
            </a>
          </div>
        </div>
      </section>

      <section class="covered-topics text-left" id="python">
        <h2>Covered topics</h2>
        <ul>
          <li>Design of the Logging module, and logger</li>
          <li>How logging messages are processed</li>
          <li>Loggers hierarchy</li>
          <li>How to configure loggers via configuration files. In this course I used a dictionary as config.</li>
          <li>Why and how to use logging filters.</li>
          <li>How to use custom logging Handlers.</li>
          <li>Creating a Telegram Bot, that will accept messages from your loggers.</li>
        </ul>
      </section>

      <section class="for-whom text-left" id="for-whom">
        <h2>For whom</h2>
        <p>The Course fits for Python developers with some experience.</p>
      </section>

      <section class="prerequisites text-left" id="prerequisites">
        <h2>Prerequisites</h2>
        <ul>
          <li>Basics of Python</li>
          <li>Understanding of Python classes, inheritance, methods overriding</li>
          <li>Linux or Mac are preferable</li>
        </ul>
      </section>


      <section class="faq text-left" id="faq">
        <h2>FAQ</h2>
        <div class="faq-wrapper">
          <div class="accordion" role="tablist">
            <b-card no-body class="mb-1" v-for="(item, index) in courseInfo.faq" :key="index">
              <b-card-header header-tag="header" class="p-1" role="tab">
                <b-button class="text-left" block v-b-toggle="`accordion-${index}`" variant="light" v-html="item.question"></b-button>
              </b-card-header>
              <b-collapse :id="`accordion-${index}`" accordion="my-accordion" role="tabpanel">
                <b-card-body>
                  <b-card-text v-html="item.answer"></b-card-text>
                </b-card-body>
              </b-collapse>
            </b-card>
          </div>
        </div>
      </section>

      <section class="text-left" id="price">
        <h2>Price</h2>
        <div class="text-center row justify-content-center">
          <CourseOfferCard
            :courseInfo="courseInfo"
          />
        </div>
      </section>

    </div>
</template>

<script>
  import { mapState } from 'vuex'

  export default {
    computed: mapState({
      courseInfo: state => state.tiers.find(tier => tier.title === 'Courses'
    ).items.find(course => course.slug === 'practical-python-logging'),
    })
  }
</script>

<style scoped>
  .hero-meta {
    font-size: 1.3rem;
    font-weight: 600;
  }
  section {
    margin-bottom: 6rem;
    font-size: 1.3rem;
  }
  section h2 {
    margin-bottom: 2rem;
    font-weight: 700;
    color: #38416f;
  }

  .course-traits {
    margin: 10rem 0;
    width: 100%;
    background: #f9fbff;
    width: 80%;
    margin: 5rem auto;
    padding: 3rem;
    border: 1px solid rgba(0, 0, 0, 0.125);
    border-radius: 10px;
  }

  .course-traits h2 {
    font-size: 5rem;
  }

  .course-traits h3 {
    font-size: 2rem;
  }

  .about span {
    display: block;
    border-left: 2px dotted grey;
    padding: 1rem 2rem;
    margin: 2rem 1rem;
    font-weight: 600;
  }

  .image-wrapper {
    border-radius: 8px;
    box-shadow: 0 10px 30px rgba(0,0,0,.2);
    width: min-content;
    margin: 1rem auto;
  }
  .video-link {
    border-bottom: 1px solid rgba(0, 0, 0, 0.05);
    text-decoration: none;
    color: #333;
    padding: 0.5rem 0;
  }
  .video-link:hover {
    background: #f9fbff;
  }

  .video-link-icon {
    margin-right: 0.5rem;
    color: #dd2e44;
  }

  .accordion {
    background: #f9fbff !important;
  }

  .accordion .card-header {
    background: #f9fbff !important;
  }

  .accordion .card-header button{
    background: #f9fbff !important;
    font-size: 1.2rem;
  }

  .faq-wrapper {
    background: #f9fbff !important;
  }

  @media(max-width: 576px) {
    .main-content {
      max-width: 90%;
    }
  }

  @media(max-width: 870px) {
    .image-wrapper {
      width: 100%;
      margin: 1rem auto;
    }

    .picture {
      width: 80%;
    }
  }

  @media (max-width: 1620px) {
    .sidebar {
      display: none;
    }
  }
</style>
