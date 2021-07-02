<template>

    <div class="col-9 mx-auto text-center">
      <div class="hero">
        <h1 class="hero-header">Practical Python: <br> Web Scraping course</h1>

        <h2 class="subheader my-4">Turn your knowledge of Python basics into a skill</h2>

        <div class="hero-meta my-4">
          3 hrs | 16 videos
        </div>

        <PatreonButton />
      </div>

      <section class="about text-left justify-content-center">
        <div class="about-content">
          <h2>What is this course about?</h2>

          <p>
            This course is about Python language, and about its application to real world tasks.<br>
          </p>
          <p>
            If you are just finished some Python tutorial like Codecademy or similar, and asked yourself:
            <span class="question">"Ok, I finished it, but what to do next? How to apply my knowledge to a real task?"</span>
            So if your are asked this question, this course is for you.
          </p>
          <p>
            During this course you will apply your Python knowledge to solve various programmers tasks.
          </p>
        </div>
        <div class="image-wrapper mt-5">
          <img src="@/assets/images/knowledge_experience.jpg" alt="" class="ml-5 mx-auto px-2">
        </div>

      </section>

      <section class="why text-left">
        <h2>Why Web Scraping?</h2>

        <p>
          Becase it's relatively simple task.
          It's fit for complete beginners in Python development.
        </p>
        <p>
          And also Web Scraping allow to earn money. That's right you will be able to earn some money with your Python Web Scraping skills.
        </p>
      </section>

      <section class="resume">
        3 hours 16 videos
      </section>

      <section class="covered-topics text-left">
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

      <section class="covered-topics text-left">
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


      <section class="for-whom text-left">
        <h2>For whom</h2>
        <p>The Practical Python: Web scraping course fit for beginners who elaborated any Python tutorial.</p>
      </section>

      <section class="prerequisites text-left">
        <h2>Prerequisites</h2>
        <ul>
          <li>Basics of Python</li>
          <li>Basics of HTML, CSS</li>
          <li>Linux or Mac Os are preferable</li>
        </ul>
      </section>


      <section class="faq text-left">
        <h2>FAQ</h2>


      </section>

    </div>
</template>

<script>
  export default {

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

  section.resume {
    margin: 10rem 0;
    width: 100%;
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
</style>
