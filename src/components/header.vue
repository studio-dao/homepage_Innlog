<template>
  <div class="header_main_container">
    <header>
      <div class="header_div_logo">
        <img
          class="header_logo"
          src="~@/assets/images/logo_innlog.png"
          alt="logo"
        />
      </div>
      <nav class="header_main_nav">
        <ul>
          <li><a href="#">LA MÉTHODE </a></li>
          <li><a href="#">NOS SOLUTIONS</a></li>
          <li><a href="#">WELCOME TO INNLOG</a></li>
          <li><a href="#">INN’LIFE</a></li>
        </ul>
      </nav>
      <div class="header_div_burger">
        <img
          @click="showModale = !showModale"
          src="@/assets/images/burger.png"
          alt="burger"
          class="header_div_burger_img"
        />
      </div>
    </header>
    <div class="header_nav_modale" v-show="showModale">
      <ul>
        <li><a href="#">LA MÉTHODE </a></li>
        <li><a href="#">NOS SOLUTIONS</a></li>
        <li><a href="#">WELCOME TO INNLOG</a></li>
        <li><a href="#">INN’LIFE</a></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",

  data() {
    return {
      showModale: false,
    };
  },

  // methods: {

  //   getNow() {
  //     const today = new Date();
  //     const date =
  //       today.getDate() +
  //       "/" +
  //       (today.getMonth() + 1) +
  //       "/" +
  //       today.getFullYear();
  //     const time =
  //       today.getHours() + ":" + today.getMinutes() + ":" + today.getSeconds();
  //     const dateTime = date + " " + time;
  //     this.timestamp = dateTime;
  //     return this.timestamp;
  //   },
  // },
};
</script>

<style scoped lang="scss">
$color1: #0078b5;
$color2: white;
$font2: "Helvetica";

.header_main_container {
  position: fixed;
  top:0px;
  z-index: 1;
  margin: 0px;
  padding: 0px;
  width: 100vw;
  header {
    display: grid;
    grid-template-columns: 1fr 2fr 1fr;
    background-color: $color1;
    padding: 10px;

    .header_div_logo {
      display: grid;
      justify-items: center;
      align-items: center;
      .header_logo {
        width: 50%;
      }
    }

    nav {
      display: grid;
      align-items: center;
      justify-items: center;
      ul {
        display: flex;
        flex-direction: row;
        list-style: none;
        margin: 0px;
        padding: 0px;
        align-items: center;
        li {
          margin: 10px;
          a {
            text-decoration: none;
            color: $color2;
            font-family: $font2;
            font-size: 0.8em;
            font-weight: bold;
          }
        }
      }
    }
    .header_div_burger {
      display: none;
    }
  }
  .header_nav_modale {
    display: none;
  }
}

//  TABLET AND MOBILE
@media (max-width: 768px) {
  $color1: #0078b5;
  $color2: white;
  $font2: "Helvetica";

  .header_main_container {
    position: fixed;
    z-index: 1;
    margin: 0px;
    padding: 0px;
    width: 100vw;
          justify-items: center;
      align-items: center;
    header {
      display: grid;
      grid-template-columns: 1fr 2fr 1fr;
      padding: 30px;
      background-color: $color1;
      height: 100px;


      .header_div_logo {

        .header_logo {
          width: 100%;
        }
      }

      nav {
        display: none;
      }
      .header_div_burger {
        display: grid;
        grid-column: 3;
        justify-items: right;
        align-items: center;
        justify-items: right;
        .header_div_burger_img {
          width: 30%;
        }
      }
    }
    .header_nav_modale {
      display: flex;
      position: absolute;
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
}
</style>
