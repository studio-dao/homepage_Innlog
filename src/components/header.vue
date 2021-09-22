<template>
  <div class="main_container">
    <header>
      <div class="div_logo">
        <img class="logo" src="~@/assets/images/logo_innlog.png" alt="logo" />
      </div>
      <nav class="main_nav">
        <ul>
          <li><a href="#">LA MÉTHODE </a></li>
          <li><a href="#">NOS SOLUTIONS</a></li>
          <li><a href="#">WELCOME TO INNLOG</a></li>
          <li><a href="#">INN’LIFE</a></li>
        </ul>
      </nav>
    </header>
  </div>
</template>

<script>
export default {
  name: "Header",

  data() {
    return {
      timestamp: "",
    };
  },

  methods: {
    getNow() {
      const today = new Date();
      const date =
        today.getDate() +
        "/" +
        (today.getMonth() + 1) +
        "/" +
        today.getFullYear();
      const time =
        today.getHours() + ":" + today.getMinutes() + ":" + today.getSeconds();
      const dateTime = date + " " + time;
      this.timestamp = dateTime;
      return this.timestamp;
    },
  },
};
</script>

<style scoped lang="scss">
$color1: #0078b5;
$color2: white;
$font1: "Courier New", Courier, monospace;
$font2: "Helvetica";
$font-weight: "bold";

@font-face {
  font-family: "Couture";
  src: url("../assets/fonts/couture-bld.otf");
}
.main_container {
  margin: 0px;
  padding:0px;
  header {
    display: grid;
    grid-template-columns: 1fr 2fr 1fr;
    background-color: $color1;
    padding: 10px;
    width: 100vw;
    .div_logo {
      display: grid;
      justify-items: center;
      align-items: center;
      .logo {
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
            font-weight: $font-weight;
          }
        }
      }
    }
  }
}
</style>
