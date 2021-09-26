<template>
  <section class="solution_main_container">
    <div class="solution_separateur"></div>
    <div class="solution_container_texte">
      <h1 class="solution_title">NOS SOLUTIONS</h1>
    </div>
    <div class="solution_caroussel_container">
      <div class="solution_carrousel_flecheLft"></div>
      <div class="solution_carrousel_flecheRght"></div>
      <div
        class="solution_carrousel_content"
        v-for="solution in solutions"
        :key="solution.id"
      >
        <div class="solution_carrousel_content_div_image">
          <img :src="solution.image" alt="Innlog solutions" />
        </div>
        <div class="solution_carrousel_content_text_div">
          <p class="solution_carrousel_content_text_div_parag">
            {{ solution.text }}
          </p>
          <p class="solution_carrousel_content_text_div_title">
            {{ solution.title }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "SectionSolutions",

  data() {
    return {
      solutions: [
        {
          image: require("@/assets/images/carroussel_nos_solutions/dev_spe.png"),
          text: " Innlog accompagne et développe votre performance numérique ",
          title: "LES DEV SPE",
        },
        {
          image: require("@/assets/images/carroussel_nos_solutions/logiciel_next.png"),
          text: " Innlog accompagne et développe votre performance numérique ",
          title: "LES LOGICIELS NEXT",
        },
        {
          image: require("@/assets/images/carroussel_nos_solutions/logiciel_tesfri.png"),
          text: " Innlog accompagne et développe votre performance numérique ",
          title: "LES LOGICIELS TESFRI",
        },
        {
          image: require("@/assets/images/carroussel_nos_solutions/solution_ecommerce.png"),
          text: " Innlog accompagne et développe votre performance numérique ",
          title: "LES SOLUTIONS E-COMMERCE",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
$color1: #0078b5;
$color2: white;
$color3: black;
$font2: "Helvetica";

.solution_main_container {
  position: relative;
  margin: 20px 0px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-items: center;

  .solution_separateur {
    width: 50px;
    background-color: $color1;
    height: 3px;
    margin: 20px 0px 50px 0px;
  }
  .solution_carrousel_flecheLft {
    position: absolute;
    top: 50%;
    left: 10px;
  }
  .solution_carrousel_flecheRght {
    position: absolute;
    top: 50%;
    right: -10px;
  }
  // CONTAINER TEXTE

  .solution_container_texte {
    display: grid;
    grid-template-columns: repeat(6, 1fr);
    .solution_title {
      display: grid;
      margin-bottom: 10px;
      grid-column: 1/7;
      margin-bottom: 50px;
      justify-content: center;
      font-family: $font2;
      font-weight: bold;
      letter-spacing: 2px;
      font-size: 2.5em;
    }
  }

  // CONTAINER CAROUSEL
  .solution_caroussel_container {
    width: 100vw;
    display: flex;
    flex-direction: row;
    align-items: center;
    .solution_carrousel_content {
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      background-color: #eee;
      .solution_carrousel_content_div_image {
        img {
          width: 100%;
          height: auto;
        }
      }
      .solution_carrousel_content_text_div {
        padding: 20px;
        font-size: 18px;
        font-weight: 300;
        .solution_carrousel_content_text_div_parag{
          line-height: 1em;
        }

        .solution_carrousel_content_text_div_title {
          color: $color1;
          font-size: 14px;
           font-weight: 700;
        }
      }
    }
  }
}
</style>
