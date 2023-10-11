<script>
import { social_menu, footer_menu } from "../data/menus";

export default {
  name: "Footer",
  data() {
    return {
      social_menu,
      footer_menu,
    };
  },
};
</script>

<template>
  <footer>
    <div class="container-csm">
      <div class="box-left">
        <div class="boolando">Boolando s.r.l</div>
        <div class="info">
          <ul>
            <li v-for="(item, index) in footer_menu" :key="`footer-${index}`">
              <a :href="item.href">{{ item.text }}</a>
            </li>
          </ul>
        </div>
      </div>

      <!-- RIGHT BOX  -->

      <div class="box-right">
        <div class="trovaci">Trovaci anche su</div>
        <div class="social">
          <ul>
            <li
              v-for="(item, index) in social_menu.footer"
              :key="`social-${index}`"
            >
              <a :href="item.href"
                ><i class="fa-brands" :class="item.icon_class"></i
              ></a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use "./scss/partials/variables" as *;

footer {
  width: 100%;
  height: 100px;
  background-color: $footer-bg-color;
  .container-csm {
    display: flex;
    justify-content: space-between;
    align-items: center;
    .box-left {
      width: 500px;
      height: 80%;
      margin-top: auto;
      margin-bottom: auto;
      .boolando {
        font-size: 20px;
        font-weight: bold;
        color: white;
        margin-top: 10px;
        margin-bottom: 10px;
      }
      .info ul {
        flex-direction: row;
        display: flex;
        gap: 10px;
        padding: 0;
        a {
          font-size: 13px;
          color: white;
        }
      }
    }
    .box-right {
      width: 500px;
      height: 80%;
      display: flex;
      flex-direction: column;
      row-gap: 10px;
      justify-content: space-around;
      align-items: end;
      .trovaci {
        margin-right: 10px;
        color: white;
      }
      ul {
        display: flex;
        flex-direction: row;
        gap: 3px;
        a {
          margin-left: 10px;
          color: $link-color;
          font-size: 20px;
        }
      }
    }
  }
}
</style>
