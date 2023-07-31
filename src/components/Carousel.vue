<script>
export default {
  name: "Carousel",
  data() {
    return {

    }
  },
  methods: {
    next() {
      this.$emit("next")
    },
    prev() {
      this.$emit("prev")
    }
  }
}
</script>

<template>
  <div class="carousel">
    <slot></slot>

    <button class="next" @click="next">Next</button>
    <button class="prev" @click="prev">Prev</button>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;

.carousel {
  position: relative;
  width: 800px;
  height: 550px;
  overflow: hidden;
  margin: 0 auto;

  button {
    position: absolute;
    height: 40px;
    width: 50px;
    top: calc(50% - 20px);
    background-color: rgba(0, 0, 0, 0.5);
    border: none;
    color: white;
  }

  button:hover {
    cursor: pointer;
  }

  .next {
    right: 0;
  }

  .prev {
    left: 0;
  }
}
</style>