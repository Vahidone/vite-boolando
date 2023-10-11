<script>
import Main from "./components/Main.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    Header,
    Footer,
    Main,
  },
};
</script>

<template>
  <Header />
  <Main />
  <Footer />
</template>

<style lang="scss">
@use "./components/scss/main.scss";
@import "bootstrap/scss/bootstrap";
</style>
