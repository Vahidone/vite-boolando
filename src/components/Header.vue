<script>
export default {
  name: "Header",
};
</script>

<template>
  <header>
    <div class="logo">
      <img src="/public/boolean-logo.png" alt="" />
    </div>
  </header>
</template>

<style scoped>
header {
  width: 100%;
  height: 70px;
  background-color: #ff6900;
  box-shadow: 0 1px 10px grey;
  position: fixed;
  z-index: 999;
}
.logo {
  width: 120px;
  height: 25px;
  margin: 25px auto;
}
img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
