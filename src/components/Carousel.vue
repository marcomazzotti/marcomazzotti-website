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

    <button href="" class="next" @click="next"><i class="fa-solid fa-arrow-right"></i></button>
    <button href="" class="prev" @click="prev"><i class="fa-solid fa-arrow-left"></i></button>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;

.carousel {
  position: relative;
  width: 900px;
  height: 500px;
  overflow: hidden;
  margin: 0 auto;
  border: 1px solid black;
  border-radius: 10px;

  button {
    position: absolute;
    top: calc(50% - 20px);
    font-size: 1.5rem;
    background-color: black;
    padding: 0.5rem;
    border: none;
    border-radius: 5px;

    i {
      color: white;
    }
  }

  button:hover {
    cursor: pointer;
    background-color: white;
    border: 1px solid black;

    i {
      color: black;
    }
  }

  .next {
    right: 16px;
    margin-right: 0.5rem;
  }

  .prev {
    left: 16px;
    margin-left: 0.5rem;
  }
}
</style>