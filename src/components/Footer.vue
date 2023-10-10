<script>
export default {
  name: "Footer",
};
</script>

<template>
  <footer>
    <div class="container-csm">
      <div class="box-left">
        <div class="boolando">Boolando s.r.l</div>
        <div class="info">
          <ul>
            <li><a href="#">Informazioni legali</a></li>
            <li><a href="#">Normativa sulla privacy</a></li>
            <li><a href="#">Diritto di recesso</a></li>
          </ul>
        </div>
      </div>

      <!-- RIGHT BOX  -->

      <div class="box-right">
        <div class="trovaci">Trovaci anche su</div>
        <div class="social">
          <ul>
            <li>
              <a href="#"><i class="fa-brands fa-square-twitter"></i></a>
            </li>
            <li>
              <a href="#"><i class="fa-brands fa-square-facebook"></i></a>
            </li>
            <li>
              <a href="#"><i class="fa-brands fa-square-instagram"></i></a>
            </li>
            <li>
              <a href="#"><i class="fa-brands fa-square-pinterest"></i></a>
            </li>
            <li>
              <a href="#"><i class="fa-brands fa-square-youtube"></i></a>
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
        a {
          font-size: 13px;
          color: $link-color;
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
          color: white;
          font-size: 20px;
        }
      }
    }
  }
}
</style>
