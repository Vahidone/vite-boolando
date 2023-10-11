<script>
export default {
  name: "ProductCard",
  props: {
    product: Object,
  },
};
</script>

<template>
  <div class="cards">
    <div class="card relative">
      <img :src="product.primaryImage" />
      <img class="replace" :src="product.secondaryImage" />
      <span v-if="!(product.discount == null)" class="discount">{{
        product.discount
      }}</span>
      <span v-if="!(product.sostenibilita == null)" class="sos">{{
        product.sostenibilita
      }}</span>
      <span class="heart">&hearts;</span>
    </div>
    <div class="subtitle">
      <p>{{ product.marca }}</p>
      <p>{{ product.modello }}</p>
      <p>
        {{ product.lastPrice }} €
        <span v-if="!(product.fullPrice == null)"
          >{{ product.fullPrice }} €</span
        >
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card .discount {
  position: absolute;
  left: 0;
  bottom: 50px;
  background-color: #ff0100;
  color: white;
  padding: 5px 8px;
}
.card .sos {
  position: absolute;
  left: 63px;
  bottom: 50px;
  background-color: #008001;
  color: white;
  padding: 5px 8px;
}

.cards:last-child .card .sos.special {
  left: 0;
}

.card .heart {
  position: absolute;
  font-size: 25px;
  right: 0;
  top: 8px;
  padding: 10px 15px;
  background-color: white;
}

.cards .subtitle p:first-child {
  color: rgb(41, 40, 40);
  font-size: 14px;
}

.cards .subtitle p:nth-child(2) {
  font-weight: bold;
}
.cards .subtitle p:last-child {
  color: #ff0100;
}
.cards .subtitle p:last-child span {
  text-decoration: line-through;
  color: black;
}

// -------------
ul {
  flex-direction: row;
  list-style: none;
}

a {
  text-decoration: none;
  color: white;
}

img {
  width: 390px;
  height: 565px;
  object-fit: cover;
}

.relative {
  position: relative;
}

/* all HOVER  */

.card .replace {
  position: absolute;
  left: 0;
  top: 0;
  opacity: 0;
}
.card .replace:hover {
  opacity: 1;
}

.card .heart:hover {
  color: red;
}
</style>
