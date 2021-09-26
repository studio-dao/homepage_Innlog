<template>
  <footer class="footer_main_container">
    <div class="footer_row_1">
      <div class="footer_logo">
        <img src="@/assets/images/logo_innlog.png" alt="" />
      </div>
      <div class="footer_col">
        <ul>
          <a href="#">
            <li>LA METHODE</li>
          </a>
          <a href="#">
            <li>NOS SOLUTIONS</li>
          </a>
          <a href="#">
            <li>NOS SERVICES</li>
          </a>
        </ul>
      </div>
      <div class="footer_col">
        <ul>
          <a href="#">
            <li>WELCOME TO INNLOG</li>
          </a>
          <a href="#">
            <li>INN'LIFE</li>
          </a>
          <a href="#">
            <li>VOUS ET NOUS</li>
          </a>
        </ul>
      </div>
      <div class="footer_col">
        <ul>
          <a href="#">
            <li>CONTACT</li>
          </a>
          <a href="#">
            <li>GROUPE TESSON</li>
          </a>
          <a href="#">
            <li>MENTIONS LEGALES</li>
          </a>
        </ul>
      </div>
    </div>
    <div class="footer_row_2">
      <img
        src="@/assets/images/pict_fcbk.png"
        alt="fbck_icon"
        class="fbk_icon"
      />
      <img
        src="@/assets/images/pict_linkedin.png"
        alt="fbck_icon"
        class="lkdin_icon"
      />
    </div>
  </footer>
</template>

<script>
export default {
  name: "Header",

  data() {
    return {
      timestamp: "",
    };
  },

};
</script>

<style scoped lang="scss">
$color1: #0078b5;
$color2: white;
$font2: "Helvetica";

.footer_main_container {
  width: 100vw;
  .footer_row_1 {
    padding: 1em;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    background-color: $color1;
    width: 100vw;
    .footer_logo {
      display: grid;
      justify-items: center;
      align-items: center;
      img {
        width: 50%;
      }
    }
    .footer_col {
      ul {
        list-style: none;
        a {
          font-family: "Helvetica";

          font-weight: 500;
          text-decoration: none;
          color: $color2;
          font-size: 16px;
          li {
            margin: 20px 0px;
          }
        }
      }
    }
  }
  .footer_row_2 {
    padding: 1em;
    display: flex;
    justify-content: center;
    background-color: $color1;
    width: 100vw;
    img{
      width: 50px;
      margin: 0px 5px;
    }
  }

}
</style>
