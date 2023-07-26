<script>
export default {
  name: "AppHeader"
}
</script>

<template>
  <div class="header py-2">
    <div class="container d-flex justify-content-between align-items-center">
      <div class="logo">
        <h1><strong>M</strong></h1>
      </div>
      <div class="menu">
        <ul class="list-unstyled d-flex">
          <li class="me-3">
            <a href="">HOME</a>
          </li>
          <li class="me-3">
            <a href="">PROJECTS</a>
          </li>
          <li class="me-3">
            <a href="">ABOUT</a>
          </li>
          <li>
            <a href="">CONTACT</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;

.header {
  border-bottom: 2px solid red;

  ul {
    margin: 0;

    a {
      padding: 0.5rem 0.9rem;
      transition: background-color 0.3s, color 0.3s;
      border-radius: 10px;
      font-size: 1.1rem;
    }

    a:hover {
      color: white;
      background-color: black;
    }
  }
}
</style>