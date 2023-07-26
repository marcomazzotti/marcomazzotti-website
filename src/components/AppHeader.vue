<script>
export default {
  name: "AppHeader"
}
</script>

<template>
  <div class="header py-2">
    <div class="container d-flex justify-content-between">
      <div class="logo">
        <h1><strong>M</strong></h1>
      </div>
      <div class="menu">
        <ul class="list-unstyled d-flex">
          <li class="me-5">
            <h6>
              <a href="">HOME</a>
            </h6>
          </li>
          <li class="me-5">
            <h6>
              <a href="">PROJECTS</a>
            </h6>
          </li>
          <li class="me-5">
            <h6>
              <a href="">ABOUT</a>
            </h6>
          </li>
          <li>
            <h6>
              <a href="">CONTACT</a>
            </h6>
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
    padding-top: 0.8rem;
  }
}
</style>