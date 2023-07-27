<script>
export default {
  name: "AppInfo"
}
</script>

<template>
  <div class="container py-5 d-flex align-items-center">
    <div class="left me-5">
      <p>Hi there, my name is Marco and I live in Milan, Italy. <br>
        I studied graphic design, but over the last few years, I developed an interest in the world of web development.
        <br>
        I've learned various front-end and back-end languages and technologies, and I enjoy using them to create beautiful
        and functional websites.</p>
    </div>
    <div class="right ms-5">
      <h2><strong>Jr. Full Stack<br>Web Developer</strong></h2>
      <button class="btn btn-primary">View Projects</button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;

.left {
  width: 50%;
  background-color: black;
  color: white;
  padding: 3rem 2rem;
  border-radius: 10px;
}

.right {
  width: 50%;

  .btn {
    border: 1px solid black !important;
    --bs-btn-bg: black;

    &:hover {
      --bs-btn-hover-bg: white !important;
      --bs-btn-hover-color: black !important;
    }
  }
}
</style>