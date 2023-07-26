<script>
export default {
  name: "AppJumbo"
}
</script>

<template>
  <div class="container my-5 d-flex align-items-center">
    <div class="left me-5">
      <h1>Hello! I'm Marco and this is my website!</h1>
    </div>
    <div class="right ms-5">
      <p class="">Welcome to my website portfolio! <br>
        My name is Marco, and I am a Junior Full Stack Web Developer. <br>
        Here you can find my projects and my personal resume. <br>
        Thank you for visiting, and have a great day!
      </p>
      <button class="btn btn-primary">Download CV</button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;

.right {
  width: 50%;
}

.left {
  width: 50%;

  h1 {
    font-size: 5rem;
  }
}

.right {
  p {
    font-size: 1.2rem;
  }
}

.btn {
  border: 1px solid black !important;
  --bs-btn-bg: black;

  &:hover {
    --bs-btn-hover-bg: white !important;
    --bs-btn-hover-color: black !important;
  }
}
</style>