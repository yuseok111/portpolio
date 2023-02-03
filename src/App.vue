<template>
  <hederS />

  <intro id="Intro" />
  <about id="About" />
  <project id="Project" />
  <cloning id="Webclon" />
  <contact id="Contact" />
</template>

<script>
import hederS from "./components/hederS.vue";
import intro from "./components/intro.vue";
import about from "./components/about.vue";
import project from "./components/project.vue";
import cloning from "./components/cloning.vue";
import contact from "./components/contact.vue";
import modal from "./components/modal.vue";

export default {
  data: () => ({
    img: require("./assets/pic.png"),
  }),
  name: "App",
  components: {
    intro,
    about,
    project,
    cloning,
    contact,
    hederS,
    modal,
  },
};
</script>

<style>
#app {
  font-family: "Roboto", "Noto Sans KR", Tahoma, Geneva, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: rgb(255, 255, 255);
}
</style>
