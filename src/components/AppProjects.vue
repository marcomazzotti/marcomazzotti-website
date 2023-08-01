<script>
import Carousel from './Carousel.vue';
import CarouselSlide from './CarouselSlide.vue';
export default {
  name: "AppProjects",
  data() {
    return {
      slides: [
        "/src/assets/Deliveroo.png",
        "/src/assets/Whatsapp.png",
        "/src/assets/Netflix.png",
        "/src/assets/Discord.png"
        // "/src/assets/1690820566206.jpeg",
        // "/src/assets/Whatsapp.jpeg",
        // "/src/assets/netflix.jpeg",
        // "/src/assets/spotify.jpeg",
      ],
      visibleSlide: 0,
      direction: ""
    }
  },
  computed: {
    slidesLen() {
      return this.slides.length
    }
  },
  methods: {
    next() {
      if (this.visibleSlide >= this.slidesLen - 1) {
        this.visibleSlide = 0
      } else {
        this.visibleSlide++
      }
      this.direction = "left"
    },
    prev() {
      if (this.visibleSlide <= 0) {
        this.visibleSlide = this.slidesLen - 1
      } else {
        this.visibleSlide--
      }
      this.direction = "right"
    },
  },
  components: {
    Carousel, CarouselSlide
  }
}
</script>

<template>
  <div class="container pt-5 text-center">
    <h2><strong>PROJECTS</strong></h2>
    <carousel @next="next" @prev="prev">
      <carousel-slide v-for="(slide, index) in slides" :key="slide" :index="index" :visibleSlide="visibleSlide"
        :direction="direction">
        <div class="carousel-image-container">
          <img :src="slide" alt="" style="width: 100%;">
        </div>
      </carousel-slide>
    </carousel>
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