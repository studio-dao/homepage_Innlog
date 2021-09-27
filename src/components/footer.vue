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
        padding: 0px;
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
    .header_div_burger{
      display: none;
    }
    .header_nav_modale{
      display: none;
    }
  }
  .footer_row_2 {
    padding: 1em;
    display: flex;
    justify-content: center;
    background-color: $color1;
    width: 100vw;
    img {
      width: 50px;
      margin: 0px 5px;
    }
  }
}
//  TABLET AND MOBILE
@media (max-width: 768px) {
  $color1: #0078b5;
  $color2: white;
  $font2: "Helvetica";

  .footer_main_container {
    position: relative;
    width: 100vw;
    .footer_row_1 {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      background-color: $color1;
      width: 100vw;
      .footer_logo {
        display: grid;
        grid-column: 2/3;
        width: 100%;
        align-items: center;
        img {
          width: 50%;
        }
      }
      .footer_col {
        display: grid;
        grid-column: 2;
        ul {
          list-style: none;
          text-align: center;
          margin: 0px;
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
      .header_div_burger {
        display: grid;
        grid-row: 1;
        grid-column: 3;
        justify-items: right;


        .header_div_burger_img {
          width: 15%;
        }
      }
      .header_nav_modale {
      display: flex;
      position: absolute;
      top: 8%;
      right: 0px;
      width: 20%;
      height: auto;
      background-color: $color2;
      ul {
        display: flex;
        flex-direction: column;
        list-style: none;
        margin: 0px;
        padding: 0px;
        align-items: left;
        li {
          margin: 10px;
          a {
            text-decoration: none;
            color: $color1;
            font-family: $font2;
            font-size: 0.8em;
            font-weight: bold;
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
      img {
        width: 50px;
        margin: 0px 5px;
      }
    }
  }
}
</style>
