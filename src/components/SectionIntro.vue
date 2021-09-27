<template>
  <div class="main_container_intro">
    <div class="image"></div>
    <div class="section_intro_droite">
      <div class="separateur_1"></div>
      <div class="title">
        CONNECTING PEOPLE & DIGITAL
      </div>
      <div class="separateur_2"></div>
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
    <div class="SectionIntro_CTA">
      <div class="CTA"><a href="#">DÉCOUVRIR LA MÉTHODE INNLOG</a></div>
    </div>
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
      padding-top: 7.4%;
  grid-template-columns: repeat(2, 1fr);

  .image {
    display: grid;
    background: url("~@/assets/images/cover.png");
    background-size: cover;
    height: auto;
  }
  .section_intro_droite {
    display: grid;
    padding-top: 10px;
    padding-left: 50px;
    align-items: center;
    .separateur_1 {
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
  .SectionIntro_CTA {
    display: grid;
    grid-row: 2;
    grid-column: 1/3;
    text-align: center;
    align-items: center;
    justify-items: center;
    .CTA {
      width: 30%;
      margin: 50px 0px;
      padding: 10px;
      font-family: "Helvetica";
      font-weight: bold;
      font-size: 1.2em;
      color: $color1;
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
}
//  TABLET AND MOBILE
@media (max-width: 768px) {
  $color1: #0078b5;
  $color2: white;
  $color3: black;
  $font2: "Helvetica";

  .main_container_intro {
    display: flex;

    width: 100vw;
    flex-direction: column;
    align-items: center;
    justify-items: center;

    .image {
      min-width: 100%;
      min-height:400px;
      background: url("~@/assets/images/cover.png");
      background-size: cover;
    }
    
    .section_intro_droite {
      padding-top: 10px;
      padding-left: 50px;
      align-items: center;
      .separateur_1{
        margin: 20px 0px 20px 0px;
        background-color: $color1;
        width: 50px;
        height: 3px;
      }
      .title {
        margin-bottom: 20px;
        max-width: 500px;
        line-height: 40px;
        font-family: $font2;
        font-weight: bold;
        font-size: 2em;
        text-align: left;
      }
       .separateur_2{
        margin: 0px 0px 20px 0px;
        background-color: $color1;
        width: 50px;
        height: 3px;
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
    .SectionIntro_CTA {
      display: grid;
      width: 700px;
      text-align: center;
      align-items: center;
      justify-items: center;
      .CTA {
        width: 50%;
        margin: 50px 0px;
        padding: 10px;
        font-family: "Helvetica";
        font-weight: bold;
        font-size: 1em;
        color: $color1;
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
  }
}
</style>
