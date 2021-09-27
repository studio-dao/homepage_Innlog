<template>
  <div class="vousnous_main_container">
    <!-- SEPARATEUR -->
    <div class="vousnous_separateur"></div>
    <!-- TITRE -->
    <div class="vousnous_title">VOUS &amp; NOUS</div>
    <!-- CHIFFRES -->
    <div class="vousnous_container_chiffres">
      <div class="vousnous_chiffres_expertise">
        <p class="expertise_chiffre">+30</p>
        <p class="expertise_subtitle">années d'expertise</p>
      </div>
      <div class="vousnous_chiffres_dev">
        <p class="dev_chiffre">60</p>
        <p class="dev_subtitle">experts et développeurs engagés</p>
      </div>
      <div class="vousnous_chiffres_projets">
        <p class="projets_chiffre">+50</p>
        <p class="projets_subtitle">projets par an</p>
      </div>
    </div>
    <!-- TEXT -->
    <div class="vousnous_text">
      <p class="vousnous_text_parag">
        En 40 ans d’accompagnement digital, nos équipes maintiennent un cap :
        l’écoute de nos clients. Nous étudions et décryptons ensemble les
        évolutions digitales spécifiques à votre secteur, à votre organisation,
        à votre stratégie. Nous vous proposons ensuite des outils adaptés pour
        relever les défis identifiés.
      </p>
    </div>
    <!-- CTA -->
    <div class="vousnous_CTA">
      <p class="vousnous_CTA_text">
        <a href="#">D&Eacute;COUVRIR NOS R&Eacute;ALISATION</a>
      </p>
    </div>
  </div>
</template>
<script>
export default {
  name: "SectionVousNous",
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
// VARIABLES
$color1: #0078b5;
$color2: white;
$color3: black;
$font2: "Helvetica";

.vousnous_main_container {
  width: 100vw;
  display: grid;
  grid-gap: 10px;

  // SEPARATEUR
  .vousnous_separateur {
    margin: 100px 0px 20px 100px;
    background-color: $color1;
    width: 50px;
    height: 3px;
  }
  //  TITRE
  .vousnous_title {
    margin: 0px 0px 70px 100px;
    max-width: 500px;
    line-height: 50px;
    font-family: $font2;
    font-weight: bold;
    font-size: 3em;
    text-align: left;
  }
  //  CHIFFRES
  .vousnous_container_chiffres {
    display: grid;
    grid-template-columns: repeat(7, 1fr);
    font-family: $font2;
    margin-bottom: 30px;
    .vousnous_chiffres_expertise {
      display: grid;
      grid-column: 2/3;
      text-align: center;
      .expertise_chiffre {
        margin: 0px;
        font-family: $font2;
        font-weight: bold;
        color: $color1;
        font-size: 5em;
      }
      .expertise_subtitle {
        margin: 0px;
        font-size: 16px;
        font-weight: lighter;
      }
    }
    .vousnous_chiffres_dev {
      display: grid;
      grid-column: 4/5;
      text-align: center;
      .dev_chiffre {
        margin: 0px;
        font-family: $font2;
        font-weight: bold;
        color: $color1;
        font-size: 5em;
      }
      .dev_subtitle {
        margin: 0px;
        font-size: 16px;
        font-weight: lighter;
      }
    }
    .vousnous_chiffres_projets {
      display: grid;
      grid-column: 6/7;
      text-align: center;
      .projets_chiffre {
        margin: 0px;
        font-family: $font2;
        font-weight: bold;
        color: $color1;
        font-size: 5em;
      }
      .projets_subtitle {
        margin: 0px;
        font-size: 16px;
        font-weight: lighter;
      }
    }
  }
  //  TEXT
  .vousnous_text {
    display: grid;
    margin-bottom: 30px;
    grid-template-columns: 1fr 6fr 1fr;
    .vousnous_text_parag {
      margin: 0px;
      display: grid;
      grid-column: 2/3;
      text-align: center;
      font-size: 16px;
      font-weight: lighter;
    }
  }
  //  CTA
  .vousnous_CTA {
    display: grid;
    justify-items: center;
    .vousnous_CTA_text {
      width: 30%;
      margin: 0px;
      padding: 10px;
      font-family: "Helvetica";
      font-weight: bold;
      font-size: 1.2em;
      color: $color1;
      text-align: center;
      align-self: center;
      border: 3px solid $color1;
      transition: transform 0.3s;
      margin-bottom: 30px;
      a {
        text-decoration: none;
        color: $color1;
      }
    }
  }
  .vousnous_CTA_text:hover {
    background-color: $color1;
    transform: scale(1.1);
    a {
      color: white;
    }
  }
}

//  TABLET AND MOBILE
@media (max-width: 768px) {
  // VARIABLES
  $color1: #0078b5;
  $color2: white;
  $color3: black;
  $font2: "Helvetica";

  .vousnous_main_container {
    width: 100vw;
    display: grid;
    grid-gap: 10px;

    // SEPARATEUR
    .vousnous_separateur {
      margin: 100px 0px 20px 100px;
      background-color: $color1;
      width: 50px;
      height: 3px;
    }
    //  TITRE
    .vousnous_title {
      margin: 0px 0px 70px 100px;
      max-width: 500px;
      line-height: 50px;
      font-family: $font2;
      font-weight: bold;
      font-size: 2em;
      text-align: left;
    }
    //  CHIFFRES
    .vousnous_container_chiffres {
      display: flex;
      flex-direction: column;
      font-family: $font2;
      margin-bottom: 30px;
      .vousnous_chiffres_expertise {
        display: grid;
        grid-column: 2/3;
        text-align: center;
        .expertise_chiffre {
          margin: 0px;
          font-family: $font2;
          font-weight: bold;
          color: $color1;
          font-size: 4em;
        }
        .expertise_subtitle {
          margin: 0px;
          font-size: 14px;
          font-weight: lighter;
        }
      }
      .vousnous_chiffres_dev {
        display: grid;
        grid-column: 4/5;
        text-align: center;
        .dev_chiffre {
          margin: 0px;
          font-family: $font2;
          font-weight: bold;
          color: $color1;
          font-size: 4em;
        }
        .dev_subtitle {
          margin: 0px;
          font-size: 14px;
          font-weight: lighter;
        }
      }
      .vousnous_chiffres_projets {
        display: grid;
        grid-column: 6/7;
        text-align: center;
        .projets_chiffre {
          margin: 0px;
          font-family: $font2;
          font-weight: bold;
          color: $color1;
          font-size: 4em;
        }
        .projets_subtitle {
          margin: 0px;
          font-size: 14px;
          font-weight: lighter;
        }
      }
    }
    //  TEXT
    .vousnous_text {
      display: grid;
      margin-bottom: 30px;
      grid-template-columns: 1fr 6fr 1fr;
      .vousnous_text_parag {
        margin: 0px;
        display: grid;
        grid-column: 2/3;
        text-align: center;
        font-size: 16px;
        font-weight: lighter;
      }
    }
    //  CTA
    .vousnous_CTA {
      display: grid;
      justify-items: center;
      .vousnous_CTA_text {
        width: 70%;
        margin: 0px;
        padding: 10px;
        font-family: "Helvetica";
        font-weight: bold;
        font-size: 1em;
        color: $color1;
        text-align: center;
        align-self: center;
        border: 3px solid $color1;
        transition: transform 0.3s;
        margin-bottom: 30px;
        a {
          text-decoration: none;
          color: $color1;
        }
      }
    }
    .vousnous_CTA_text:hover {
      background-color: $color1;
      transform: scale(1.1);
      a {
        color: white;
      }
    }
  }
}

//  TABLET AND MOBILE
@media (max-width: 768px) {


}
</style>
