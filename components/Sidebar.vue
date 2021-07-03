<template>
  <div class="sidebar">
    <ul class="text-left">
      <li>
        <a href="/courses/practical-python-web-scraping#about">About</a>
      </li>
      <li><a href="/courses/practical-python-web-scraping#why">Why Web Scraping</a></li>
      <li><a href="/courses/practical-python-web-scraping#index">Index</a></li>
      <li><a href="/courses/practical-python-web-scraping#python">Covered Python topics</a></li>
      <li><a href="/courses/practical-python-web-scraping#scraping">Covered Web Scraping topics</a></li>
      <li><a href="/courses/practical-python-web-scraping#for-whom">For Whom</a></li>
      <li><a href="/courses/practical-python-web-scraping#prerequisites">Prerequisites</a></li>
      <li><a href="/courses/practical-python-web-scraping#faq">FAQ</a></li>
      <li><a href="/courses/practical-python-web-scraping#price">Price</a></li>
    </ul>
  </div>
</template>

<script>
  export default {

  }
</script>

<style scoped>
  .sidebar {
    position: fixed;
    top: 200px;
    left: 100px;
    background: #f5f9fb;
    border-radius: 16px;
    border: 1px solid rgba(0, 0, 0, 0.125);
    overflow: hidden;
  }

  .sidebar ul {
    font-size: 1rem;
    list-style: none;
    margin: 0;
    padding: 0;
  }

  .sidebar ul li {
    border-bottom: 1px solid rgba(0, 0, 0, 0.125);
  }

  .sidebar ul li:last-child {
    border-bottom: none;
  }

  .sidebar ul li:hover {
    background: rgba(62, 123, 154, 0.12);
  }

  .sidebar ul li a {
    border-radius: 16px;
    display: block;
    padding: 1rem 2rem;
    text-decoration: none;
    color: #333;
  }

  .sidebar ul li a:hover {
    color: #da3654;
    border-radius: 16px;
  }

  .sidebar ul li a.active {
    color: #da3654;
  }

</style>
