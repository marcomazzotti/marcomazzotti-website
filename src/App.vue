<script>
import AppHeader from './components/AppHeader.vue';
import AppJumbo from './components/AppJumbo.vue';
export default {
  components: { AppHeader, AppJumbo }
}
</script>

<template>
  <AppHeader />
  <AppJumbo />
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>