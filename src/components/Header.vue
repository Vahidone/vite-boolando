<script>
import { main_menu, social_menu } from "../data/menus";
export default {
  name: "Header",
  data() {
    return {
      main_menu,
      social_menu,
    };
  },
};
</script>

<template>
  <header>
    <div class="container-csm">
      <!-- MENU di sinistra del header  -->
      <div class="menu">
        <ul>
          <li v-for="(item, index) in main_menu" :key="`main-${index}`">
            <a :href="item.href">{{ item.text }}</a>
          </li>
        </ul>
        <!-- LOGO del header  -->
      </div>
      <div class="logo">
        <img src="/public/boolean-logo.png" alt="" />
      </div>

      <!-- LOGIN del header  -->
      <div class="login">
        <ul>
          <li
            v-for="(item, index) in social_menu.header"
            :key="`login-${index}`"
          >
            <a :href="item.href"><i :class="item.icon_class"></i></a>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "./scss/partials/variables" as *;
header {
  width: 100%;
  height: 70px;
  background-color: $header-bg-color;
  box-shadow: 0 1px 10px grey;
  .container-csm {
    display: flex;
    align-items: center;
  }
}

.logo {
  width: 120px;
  height: 25px;
  margin: 25px auto;
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}

li {
  display: inline-block;
  margin-right: 10px;
  a {
    color: $link-color;
    text-transform: capitalize;
    text-decoration: none;
    &:hover {
      color: lighten($link-color, 70%);
      text-decoration: underline;
    }
  }
}
</style>
