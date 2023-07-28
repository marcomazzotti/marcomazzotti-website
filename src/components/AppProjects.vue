<script>
export default {
  name: "AppProjects",
  data() {
    return {
      sliderProjects: [
        {
          name: "Deliveboo",
          image: "../assets/deliveboo.png"
        },
        {
          name: "Whatsapp",
          image: "../assets/whatsapp.jpeg"
        },
        {
          name: "Spotify",
          image: "../assets/spotify.jpeg"
        },
        {
          name: "Netflix",
          image: "../assets/netflix.jpeg"
        },
      ]
    }
  }
}
</script>

<template>
  <div class="container py-5 text-center">
    <h2><strong>PROJECTS</strong></h2>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;

.container {
  border-bottom: 1px solid red;

  h2 {
    font-size: 2rem;
  }
}
</style>