<script>
import ProductCard from "./partials/ProductCard.vue";
import products from "../data/products";

export default {
  name: "Main",
  components: {
    ProductCard,
    products,
  },
  data() {
    return {
      products,
    };
  },
};
</script>

<template>
  <main class="container-csm d-flex">
    <!-- ROW --- -->
    <div class="row-top d-flex">
      <ProductCard
        v-for="product in products"
        :key="product.id"
        :product="product"
      />
    </div>
  </main>
</template>

<style lang="scss">
@use "./scss/partials/variables" as *;

main {
  flex-flow: column wrap;
  padding-top: 50px;
  padding-bottom: 50px;
  gap: 80px;
  .row-top {
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-top: 70px;
    gap: 10px;
  }
  .row-down {
    flex-direction: row;
    justify-content: space-between;
    gap: 10px;
  }
}
</style>
