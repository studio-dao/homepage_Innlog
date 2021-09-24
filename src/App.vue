<template>
  <div id="app">
    <Header/>
    <SectionIntro/>
    <SectionExpertise/>
    <SectionSolutions/>
    <Footer/>
  </div>
</template>

<script>
import Header from "./components/header.vue";
import SectionIntro from "./components/SectionIntro.vue"
import SectionExpertise from "./components/SectionExpertise.vue"
import SectionSolutions from "./components/SectionSolutions.vue"
import Footer from "./components/footer.vue"

export default {
  name: "App",
  components: {
    Header,
    SectionIntro,
    SectionExpertise,
    SectionSolutions,
    Footer
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  margin: 0px;
  padding: 0px;
}
</style>
