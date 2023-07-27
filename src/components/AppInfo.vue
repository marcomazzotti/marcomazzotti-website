<script>
export default {
  name: "AppInfo"
}
</script>

<template>
  <div class="container py-5 d-flex align-items-center">
    <div class="left me-5">
      <div class="img-container pb-5">
        <img src="../assets/Foto Social.jpeg" alt="">
      </div>
      <p class="px-4">Hi there, my name is Marco and I live in Milan, Italy. <br>
        I studied graphic design, but over the last few years, I developed an interest in the world of web development.
        <br>
        I've learned various front-end and back-end languages and technologies, and I enjoy using them to create modern
        and functional websites.
      </p>
    </div>
    <div class="right ms-5">
      <h2><strong>Jr. Full Stack<br>Web Developer</strong></h2>
      <button class="btn btn-primary">View Projects</button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;

.container {
  border-bottom: 1px solid red;
}

.left {
  width: 50%;
  background-color: black;
  padding: 4rem 3rem;
  border-radius: 10px;
  margin-top: 1.5rem;
  margin-bottom: 1.5rem;

  p {
    font-size: 1.1rem;
    color: white;
  }

  .img-container {
    text-align: end;
  }

  img {
    max-width: 40%;
    border-radius: 50%;
  }
}

.right {
  width: 50%;
  margin-top: 1.5rem;
  margin-bottom: 1.5rem;

  h2 {
    font-size: 3rem;
  }

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