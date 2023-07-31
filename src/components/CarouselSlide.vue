<script>
export default {
  name: "CarouselSlide",
  props: ["visibleSlide", "index", "direction"],
  data() {
    return {

    }
  }
}
</script>

<template>
  <transition :name="direction" mode="in-out">
    <div v-show="visibleSlide === index" class="carousel-slide">
      <slot></slot>
    </div>
  </transition>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;

.carousel-slide {
  position: absolute;
  left: 0;
  right: 0;
  left: 0;
  bottom: 0;
}

.left-enter-active {
  animation: LeftInAnimation 0.4s ease-in-out;
}

.left-leave-active {
  animation: LeftOutAnimation 0.4s ease-in-out;
}

@keyframes LeftInAnimation {
  from {
    transform: translateX(100%);
  }

  to {
    transform: translateX(0);
  }
}

@keyframes LeftOutAnimation {
  from {
    transform: translateX(0);
  }

  to {
    transform: translateX(-100%);
  }
}

.right-enter-active {
  animation: RightInAnimation 0.4s ease-in-out;
}

.right-leave-active {
  animation: RightOutAnimation 0.4s ease-in-out;
}

@keyframes RightInAnimation {
  from {
    transform: translateX(-100%);
  }

  to {
    transform: translateX(0);
  }
}

@keyframes RightOutAnimation {
  from {
    transform: translateX(0);
  }

  to {
    transform: translateX(100%);
  }
}
</style>