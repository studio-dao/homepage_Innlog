<template>
  <div class="main_container_expertise">
    <!-- PARTIE GAUCHE -->

    <div class="container_carrousel">
      <div class="bouton boutonlft" @click="prev()"></div>
      <div class="bouton boutonrght" @click="next()"></div>
      <div
        class="carroussel"
        v-for="domaine in domaines"
        :key="domaine.index"
        :style="{ transform: `translateX(${data}px)` }"
      >
        <div class="container_domaine">
          <h3 class="titre_blanc">{{ domaine.title }}</h3>
          <img :src="domaine.image" alt="domaine.title" />
          <div class="div_infos">
            <h3 class="titre_overlay">{{ domaine.title }}</h3>
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
      data: 0,
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

  methods: {
    prev() {
      console.log(this.data);
      if (this.data === -1250) {
        this.data = 0;
      } else {
        this.data -= 200;
      }
    },

    next() {
      console.log(this.data);
      if (this.data === 1250) {
        this.data = 0;
      } else {
        this.data += 200;
      }
    },
  },
};
</script>

<style scoped lang="scss">
$color1: #0078b5;
$color2: white;
$color3: black;
$font2: "Helvetica";


.main_container_expertise {
  display: grid;
  padding: 2em 1em;
  grid-template-columns: repeat(2, 1fr);
  background-color: $color1;

  /* DIV CARROUSEL */
  .container_carrousel {
    position: relative;
    display: flex;
    flex-direction: row;
    justify-items: center;
    align-items: center;
    width: 550px;
    overflow: hidden;
    .bouton {
      position: absolute;
      top: 50%;
      z-index: 1;
      width: 20px;
      height: 20px;
      border-top: 3px solid white;
      border-right: 3px solid white;
    }
    .boutonlft {
      left: 15px;
      transform: rotate(-135deg);
    }
    .boutonrght {
      right: 15px;
      transform: rotate(45deg);
    }
    .carroussel {
      width: 200px;
      height: 400px;
      .container_domaine {
        display: inline-block;
        justify-items: left;
        position: relative;
        padding: 0px 5px;
        width: 190px;
        height: 400px;
        overflow: hidden;
        img {
          z-index: 2;
          display: block;
          width: 100%;
        }
        .titre_blanc {
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
          font-size: 12px;
          font-weight: 100;
          background: $color2;
          color: $color1;
          .titre_overlay {
            font-family: "Helvetica";
            font-size: 16px;
          }
        }
        .div_infos:hover {
          opacity: 1;
        }
      }
    }
  }
  // PARTIE DROITE
  .separateur {
    margin-bottom: 20px;
    background-color: $color2;
    width: 50px;
    height: 3px;
  }
  .text_droite {
    padding: 20px;
    text-align: left;
    color: $color2;
    font-family: "Helvetica";
    font-weight: lighter;
  }

  h1 {
    max-width: 300px;
    font-family: $font2;
    font-size: 3em;
    font-weight: bold;
    letter-spacing: 2px;
  }
}
</style>
