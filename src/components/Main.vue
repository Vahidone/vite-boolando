<script>
export default {
  name: "Main",
};
</script>

<template>
  <main class="container-csm d-flex">
    <!-- ROW 1  -->
    <div class="row-top d-flex">
      <div class="cards">
        <div class="card relative">
          <img src="/1.webp" />
          <img class="replace" src="/1b.webp" />
          <span class="discount">- 50%</span>
          <span class="sos">Sostenibilità</span>
          <span class="heart">&hearts;</span>
        </div>
        <div class="subtitle">
          <p>Levi's</p>
          <p>RELAXED FIT TEE UNISEX</p>
          <p>14,99 € <span>29,99 €</span></p>
        </div>
      </div>

      <div class="cards">
        <div class="card relative">
          <img src="/2.webp" />
          <img class="replace" src="/2b.webp" />
          <span class="discount">- 30%</span>
          <span class="heart">&hearts;</span>
        </div>
        <div class="subtitle">
          <p>Guess</p>
          <p>ROSES TEE</p>
          <p>20,99 € <span>29,99 €</span></p>
        </div>
      </div>

      <div class="cards">
        <div class="card relative">
          <img src="/3.webp" />
          <img class="replace" src="/3b.webp" />
          <span class="discount">- 30%</span>
          <span class="heart">&hearts;</span>
        </div>
        <div class="subtitle">
          <p>Come Zucchero Filiato</p>
          <p>VOGLIA DI COLORI PASTELLO</p>
          <p>129,99 € <span>184,99 €</span></p>
        </div>
      </div>
    </div>

    <!-- ROW 2  -->

    <div class="row-down d-flex">
      <div class="cards">
        <div class="card relative">
          <img src="/4.webp" />
          <img class="replace" src="/4b.webp" />
          <span class="discount">- 50%</span>
          <span class="sos">Sostenibilità</span>
          <span class="heart">&hearts;</span>
        </div>
        <div class="subtitle">
          <p>Levi's</p>
          <p>TEE UNISEX</p>
          <p>14,99 € <span>29,99 €</span></p>
        </div>
      </div>

      <div class="cards">
        <div class="card relative">
          <img src="/5.webp" />
          <img class="replace" src="/5b.webp" alt="" />
          <span class="heart">&hearts;</span>
        </div>
        <div class="subtitle">
          <p>Maya Deluxe</p>
          <p>STRIPE BODICE</p>
          <p>99,99 €</p>
        </div>
      </div>

      <div class="cards">
        <div class="card relative">
          <img src="/6.webp" />
          <img class="replace" src="/6b.webp" />
          <span class="sos special">Sostenibilità</span>
          <span class="heart">&hearts;</span>
        </div>
        <div class="subtitle">
          <p>Esprit</p>
          <p>MAGLIONE - BLACK</p>
          <p>29,99 €</p>
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "./scss/partials/variables" as *;

main {
  flex-flow: column wrap;
  padding-top: 50px;
  padding-bottom: 50px;
  gap: 80px;
  .row-top {
    flex-direction: row;
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

.container-csm .card .discount {
  position: absolute;
  left: 0;
  bottom: 50px;
  background-color: #ff0100;
  color: white;
  padding: 5px 8px;
}
.container-csm .card .sos {
  position: absolute;
  left: 63px;
  bottom: 50px;
  background-color: #008001;
  color: white;
  padding: 5px 8px;
}

.row-down .cards:last-child .card .sos.special {
  left: 0;
}

.container-csm .card .heart {
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

.container-csm .card .heart:hover {
  color: red;
}
</style>
