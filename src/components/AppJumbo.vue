<script>
export default {
  name: "AppJumbo"
}
</script>

<template>
  <div class="wrapper py-5">
    <div class="container pt-5 text-center">
      <div class="infos">
        <h1 class="pt-5"><strong>CIAO, SONO MARCO MAZZOTTI</strong></h1>
        <h4 class="pt-4">Junior Full-Stack Web Developer</h4>
        <div class="mt-5 pb-5">
          <a href="">PROGETTI</a>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;

.wrapper {
  background-image: linear-gradient(rgba(255, 255, 255, 0.6), rgba(255, 255, 255, 0.6)), url(../assets/hero-bg.svg);
}

a {
  background-color: rgb(118, 194, 175);
  padding: 0.7rem 3rem;
  border-radius: 5px;
  color: white;
  box-shadow: 0 5px 15px 0 rgba(0, 0, 0, .3);
}
</style>