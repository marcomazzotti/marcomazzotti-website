<script>
export default {
  name: "AppHeader",
  data() {
    return {
      menuList: [
        {
          name: "HOME",
          id: "home"
        },
        {
          name: "ABOUT",
          id: "about"
        },
        {
          name: "PROJECTS",
          id: "projects"
        },
        {
          name: "CONTACT",
          id: "contact"
        }
      ]
    }
  }
}
</script>

<template>
  <div class="header py-2">
    <div class="container d-flex justify-content-between align-items-center">
      <div class="logo">
        <h1><strong>M</strong></h1>
      </div>
      <div class="menu">
        <ul class="list-unstyled d-flex">
          <li v-for="(item, index) in menuList" :key="index" :class="{ 'me-3': index < menuList.length - 1 }">
            <a :href="`#${item.id}`">{{ item.name }}</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;

.header {
  border-bottom: 2px solid red;
  position: fixed;
  width: 100%;
  height: 70px;
  background-color: white;

  ul {
    margin: 0;

    a {
      padding: 0.5rem 0.9rem;
      transition: background-color 0.3s, color 0.3s;
      border-radius: 10px;
      font-size: 1.1rem;
    }

    a:hover {
      color: white;
      background-color: black;
    }
  }
}
</style>