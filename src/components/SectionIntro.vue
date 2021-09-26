<template>
  <div class="main_container_intro">
    <div class="image"></div>
    <div class="section_intro_droite">
      <div class="separateur"></div>
      <div class="title">
        CONNECTING PEOPLE & DIGITAL
      </div>
      <div class="separateur"></div>
      <p>
        Innlog accompagne et développe votre performance numérique grâce à des
        solutions adaptées et un accompagnement global, déployés dans le temps.
        En amont de chaque projet, nos consultants, experts et chefs de projet
        étudient avec vous les contraintes, mais aussi les opportunités propres
        à votre organisation. Ensemble, nous définissons la stratégie et les
        moyens pour satisfaire votre ambition et garantir ainsi le bon
        déploiement comme la bonne utilisation de vos nouveaux outils.
      </p>
      <a href="#">
        <p>
          DÉCOUVRIR NOS SOLUTIONS
        </p>
      </a>
    </div>
    <div class="CTA"><a href="#">DÉCOUVRIR LA MÉTHODE INNLOG</a></div>
  </div>
</template>

<script>
export default {
  name: "SectionIntro",

  data() {
    return {};
  },
};
</script>

<style scoped lang="scss">
// VARIABLES
$color1: #0078b5;
$color2: white;
$color3: black;
$font2: "Helvetica";

.main_container_intro {
  display: grid;
  grid-template-columns: repeat(10, 1fr);
  grid-template-rows: 1fr 0.3fr;
  grid-auto-rows: minmax(50px, 1fr);

  .image {
    display: grid;
    grid-column: 1/6;
    background: url("~@/assets/images/cover.png");
    background-size: cover;
  }
  .section_intro_droite {
    display: grid;
    grid-column: 6/12;
    padding-top: 10px;
    padding-left: 50px;
    align-items: center;
    .separateur {
      margin-bottom: 20px;
      background-color: $color1;
      width: 50px;
      height: 3px;
    }
    .title {
      margin-bottom: 20px;
      max-width: 500px;
      line-height: 50px;
      font-family: $font2;
      font-weight: bold;
      font-size: 3em;
      text-align: left;
    }
    a {
      text-decoration: none;
      p {
        font-family: "Helvetica";
        font-size: 1em;
        color: $color1;
        transition: letter-spacing 0.5s;
      }
      p:hover {
        letter-spacing: 2px;
      }
    }
  }
  .CTA {
    display: grid;
    margin: 50px 0px;
    padding: 10px;
    grid-column: 4/8;
    font-family: "Helvetica";
    font-weight: bold;
    font-size: 1.2em;
    color: $color1;
    text-align: center;
    align-items: center;
    border: 3px solid $color1;
    transition: transform 0.3s;
    a {
      text-decoration: none;
      color: $color1;
    }
  }
  .CTA:hover {
    background-color: $color1;
    transform: scale(1.1);
    a {
      color: white;
    }
  }
}
</style>
