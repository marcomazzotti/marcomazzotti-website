<script>
export default {
  name: "AppHeader"
}
</script>

<template>
  <div class="container">
    <div class="header d-flex align-items-center justify-content-between">
      <div class="img-container d-flex">
        <!-- <img src="" alt="Immagine di prova"> -->
        <h5 class="mx-4"><a href="">MARCO MAZZOTTI</a></h5>
      </div>
      <div class="right-header pt-3">
        <ul class="d-flex list-unstyled align-items-center justify-content-center">
          <li class="mx-4">
            <h5><a href="">HOME</a></h5>
          </li>
          <li class="mx-4">
            <h5><a href="">ABOUT</a></h5>
          </li>
          <li class="mx-4">
            <h5><a href="">PROJECTS</a></h5>
          </li>
          <li class="mx-4">
            <h5><a href="">CONTACT</a></h5>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;

h5:hover {
  color: rgb(118, 194, 175);
}
</style>