<template>
  <div class="sidebar">
    <ul class="text-left">
      <li v-for="(section, index) in courseInfo.sections" :key="index">
        <a :href="`/courses/${courseInfo.slug}#${section.ref}`">{{section.title}}</a>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    props: [
      'courseInfo'
    ]
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
