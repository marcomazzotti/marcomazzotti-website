<script>
import AppContacts from './components/AppContacts.vue';
import AppHeader from './components/AppHeader.vue';
import AppInfo from './components/AppInfo.vue';
import AppJumbo from './components/AppJumbo.vue';
import AppProjects from './components/AppProjects.vue';
export default {
  components: { AppHeader, AppJumbo, AppInfo, AppProjects, AppContacts }
}
</script>

<template>
  <AppHeader />
  <AppJumbo />
  <AppInfo />
  <AppProjects />
  <AppContacts />
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>