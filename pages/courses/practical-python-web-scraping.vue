<template>

    <div class="main-content col-lg-9 col-md-11 col-sm-12 mx-auto text-center">
      <div class="hero">
        <h1 class="hero-header">Practical Python: <br> Web Scraping course</h1>

        <h2 class="subheader my-4">Turn your knowledge of Python basics into a skill</h2>

        <div class="hero-meta my-4 mb-5">
          3 hrs | 16 videos
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
            This course is about Python language, and about its application to real world tasks.<br>
          </p>
          <p>
            If you are just finished some Python tutorial like Codecademy or similar, and asked yourself:
            <span class="question">"Ok, I finished it, but what to do next? How to apply my knowledge to a real task?"</span>
            So if you asked this question, this course is for you.
          </p>
          <p>
            During this course you will apply your Python knowledge, solving various programing tasks to achieve Web Scraping goals.
          </p>
        </div>
        <div class="image-wrapper mt-5">
          <img src="@/assets/images/knowledge_experience.jpg" alt="" class="ml-5 mx-auto px-2 picture">
        </div>

      </section>

      <section class="why text-left" id="why">
        <h2>Why Web Scraping?</h2>
        <p>
          First of all, Web Scraping is an automated gathering data from websites.
        </p>
        <p>
          It's a relatively simple programming task, which fits for complete beginners in Python development.
        </p>
        <p>
          It's the next step in your progress as a Python developer, if you completed any Python tutorial. All your further knowledge and experience will be built upon the skill you'll get as the result of this course.
        </p>
        <p>
          And also Web Scraping allows you to earn money. That's right! You will be able to earn some money with your Python Web Scraping skills.
        </p>
      </section>

      <section class="course-traits row justify-content-center">
        <div class="col-md-5">
          <h2 class="mb-3">3</h2>
          <h3>hours</h3>
        </div>
        <div class="col-md-5">
          <h2 class="mb-3">16</h2>
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
        <h2>Covered Python topics</h2>
        <ul>
          <li>The <code>if __name__ == '__main__'</code> - what is it and how to use it</li>
          <li>Using of <code>for</code> and <code>while</code> loops</li>
          <li>List comprehensions</li>
          <li>Usage of lists and dictionaries</li>
          <li>Writing dictionaries to CSV files</li>
          <li>Using of <code>.append()</code> and <code>.extend()</code> list methods</li>
          <li>Handling exceptions with <code>try...except...</code> block</li>
          <li>Using of <code>else</code> clause of <code>try... except...</code></li>
          <li>Functions</li>
          <li>Using of <code>map()</code> function</li>
          <li>Difference between multi-threading and multi-processing and using of both</li>
        </ul>
      </section>

      <section class="covered-topics text-left" id="scraping">
        <h2>Covered Web Scraping topics</h2>
        <ul>
          <li>Using of Requests library and BeatifulSoup</li>
          <li>How to use proxies with Requests</li>
          <li>How to scrape websites with pagination (2 methods)</li>
          <li>How to change User-Agent of your scrapers</li>
          <li>Reading and writing data to CSV files</li>
          <li>Writing data to PostgreSQL with PeeWee library</li>
          <li>Performance improving: using of multi-threading</li>
          <li>Performance improving: using of multi-processing</li>
          <li>How to scrape AJAX and JQuery driven websites</li>
        </ul>
      </section>


      <section class="for-whom text-left" id="for-whom">
        <h2>For whom</h2>
        <p>The Course fits for beginners who elaborated any Python tutorial.</p>
      </section>

      <section class="prerequisites text-left" id="prerequisites">
        <h2>Prerequisites</h2>
        <ul>
          <li>Basics of Python</li>
          <li>Basics of HTML, CSS</li>
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
        ).items.find(course => course.slug === 'practical-python-web-scraping'),
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
