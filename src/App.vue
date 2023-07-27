<script>
import AppHeader from './components/AppHeader.vue';
import AppInfo from './components/AppInfo.vue';
import AppJumbo from './components/AppJumbo.vue';
export default {
  components: { AppHeader, AppJumbo, AppInfo }
}
</script>

<template>
  <AppHeader />
  <AppJumbo />
  <AppInfo />
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>