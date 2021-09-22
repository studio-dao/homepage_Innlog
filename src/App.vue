<template>
  <div id="app">
    <Header/>
    <SectionIntro/>
    <SectionExpertise/>
  </div>
</template>

<script>
import Header from "./components/header.vue";
import SectionIntro from "./components/SectionIntro.vue"
import SectionExpertise from "./components/SectionExpertise.vue"

export default {
  name: "App",
  components: {
    Header,
    SectionIntro,
    SectionExpertise
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
