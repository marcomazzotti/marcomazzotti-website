<script>
import Carousel from './Carousel.vue';
import CarouselSlide from './CarouselSlide.vue';
export default {
  name: "AppProjects",
  data() {
    return {
      slides: [
        {
          name: "Deliveroo",
          image: "/src/assets/Deliveroo.png",
        },
        {
          name: "Whatsapp",
          image: "/src/assets/Whatsapp.png",
        },
        {
          name: "Netflix",
          image: "/src/assets/Netflix.png",
        },
        {
          name: "Discord",
          image: "/src/assets/Discord.png"
        },
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
  <div class="container py-5 text-center" id="projects">
    <h2 class="pb-5"><strong>PROJECTS</strong></h2>
    <carousel @next="next" @prev="prev">
      <carousel-slide v-for="(slide, index) in slides" :key="slide" :index="index" :visibleSlide="visibleSlide"
        :direction="direction">
        <div class="carousel-image-container">
          <img :src="slide.image" alt="" style="width: 100%; border-radius: 10px; object-fit: contain;">
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

.carousel-slide {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100%;
  border-radius: 100px;
}

.carousel-image-container {
  max-width: 100%;
  max-height: 100%;
}
</style>