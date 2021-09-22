<template>
  <div class="main_container_expertise">
    <!-- PARTIE GAUCHE -->
    <div class="container_carrousel">
      <div class="carroussel" v-for="domaine in domaines" :key="domaine.index">
        <div class="container_domaine">
          <h3 class="titre_blanc">{{ domaine.title }}</h3>
          <img :src="domaine.image" alt="domaine.title" />
          <div class="div_infos">
            <h3>{{ domaine.title }}</h3>
            <p>{{ domaine.text }}</p>
          </div>
        </div>
      </div>
    </div>
    <!-- PARTIE DROITE -->
    <div class="text_droite">
      <div class="separateur"></div>
      <h1>NOS DOMAINES D'EXPERTISE</h1>
      <p>
        L’histoire entrepreneuriale et centenaire du Groupe Tesson permet à
        Innlog de matérialiser l’expertise accumulée dans différents domaines en
        outils de performances commerciale, administrative et logistique.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionExpertise",

  data() {
    return {
      domaines: [
        {
          image: require("@/assets/images/nos_domaines_d_expertise/le_froid.png"),
          title: "Le Froid",
          text:
            "L’histoire entrepreneuriale et centenaire du Groupe Tesson permet à Innlog de matérialiser l’expertise accumulée dans différents domaines en outils de performances commerciale, administrative et logistique.",
        },
        {
          image: require("@/assets/images/nos_domaines_d_expertise/le_vin.png"),
          title: "le vin",
          text:
            "L’histoire entrepreneuriale et centenaire du Groupe Tesson permet à Innlog de matérialiser l’expertise accumulée dans différents domaines en outils de performances commerciale, administrative et logistique.",
        },
        {
          image: require("@/assets/images/nos_domaines_d_expertise/la_logistique.png"),
          title: "La Logistique",
          text:
            "L’histoire entrepreneuriale et centenaire du Groupe Tesson permet à Innlog de matérialiser l’expertise accumulée dans différents domaines en outils de performances commerciale, administrative et logistique.",
        },
        {
          image: require("@/assets/images/nos_domaines_d_expertise/le_e_commerce.png"),
          title: "E-Commerce",
          text:
            "L’histoire entrepreneuriale et centenaire du Groupe Tesson permet à Innlog de matérialiser l’expertise accumulée dans différents domaines en outils de performances commerciale, administrative et logistique.",
        },
        {
          image: require("@/assets/images/nos_domaines_d_expertise/l_industrie.png"),
          title: "Industrie",
          text:
            "L’histoire entrepreneuriale et centenaire du Groupe Tesson permet à Innlog de matérialiser l’expertise accumulée dans différents domaines en outils de performances commerciale, administrative et logistique.",
        },
        {
          image: require("@/assets/images/nos_domaines_d_expertise/l_agroalimentaire.png"),
          title: "L'Agroalimentaire",
          text:
            "L’histoire entrepreneuriale et centenaire du Groupe Tesson permet à Innlog de matérialiser l’expertise accumulée dans différents domaines en outils de performances commerciale, administrative et logistique.",
        },
      ],
    };
  },

  methods: {},
};
</script>

<style scoped lang="scss">
$color1: #0078b5;
$color2: white;
$color3: black;
$font1: "Courier New", Courier, monospace;
$font2: "Helvetica";
@font-face {
  font-family: "Couture";
  src: url("../assets/fonts/couture-bld.otf");
}

.main_container_expertise {
  display: grid;
  padding-top: 2em;
  grid-template-columns: repeat(2, 1fr);
  background-color: $color1;
  .separateur {
    background-color: $color2;
    width: 50px;
    height: 3px;
  }

  /* DIV CARROUSEL */
  .container_carrousel {
    .carroussel {
      width: 200px;
      height: 400px;
      margin: 0px 5px;
      display: inline-block;
      .container_domaine {
        display: inline-block;
        position: relative;
        width: 200px;
        height: 400px;
        overflow: hidden;
        img {
          z-index: 2;
          display: block;
          width: 100%;
        }
        .titre_blanc{
          position: absolute;
          top: 11px;
          left: 11px;
          font-family: "Helvetica";
          text-transform: uppercase;
          font-size: 16px;
          color: $color2;
        }
        .div_infos {
          position: absolute;
          padding: 10px;
          top: 0;
          bottom: 0;
          left: 0;
          right: 0;
          height: 100%;
          width: 100%;
          opacity: 0;
          transition: 0.5s ease;
          font-family: "Helvetica";
          text-transform: uppercase;
          font-size: 14px;
          font-weight: 100;
          background: $color2;
          color: $color1;
        }
        .div_infos:hover{
          opacity: 1;
        }
      }
    }
  }
  // PARTIE DROITE
  .text_droite {
    padding: 20px;
    text-align: left;
    color: $color2;
    font-family: "Helvetica";
    font-weight: 100;
  }

  h1 {
    max-width: 300px;
    font-size: 3em;
  }
}
</style>
