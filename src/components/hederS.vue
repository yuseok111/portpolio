<template>
  <nav
    :class="{
      original_color: scrollPosition < 870,
      change_color: scrollPosition > 900,
      change2_color: scrollPosition > 2300,
      change4_color: scrollPosition > 5500,
    }"
  >
    <ul>
      <li @click="goSection" data-target="Intro" class="gotosecs">INTRO</li>
      <li @click="goSection" data-target="About" class="gotosecs">ABOUT</li>
      <li @click="goSection" data-target="Project" class="gotosecs">PROJECT</li>
      <li @click="goSection" data-target="Webclon" class="gotosecs">CLONE</li>
      <li @click="goSection" data-target="Contact" class="gotosecs">CONTACT</li>
    </ul>
  </nav>
</template>
<script>
export default {
  name: "Header",
  data() {
    return {
      scrollPosition: null,
    };
  },
  methods: {
    updateScroll() {
      this.scrollPosition = window.scrollY;
    },
    goSection(e) {
      const sec = document.getElementById(e.target.dataset.target);
      if (sec) {
        sec.scrollIntoView({ behavior: "smooth" });
      }
    },
  },
  mounted() {
    window.addEventListener("scroll", this.updateScroll);
  },
};
</script>
<style scoped>
nav {
  position: fixed;
  color: #d9d9d9;
  z-index: 1000;
  text-align: center;
  left: 80%;
}
nav ul {
  justify-content: flex-end;
}
nav ul li {
  float: left;
  padding: 7px;
  font-weight: bold;
  font-size: 16px;
}
.original_color {
  position: fixed;
  color: #fff;
  width: 100%;
}

.change_color {
  position: fixed;

  color: #000;
  width: 100%;
}
.change2_color {
  position: fixed;
  color: rgb(211, 12, 12);
  width: 100%;
}
.change4_color {
  position: fixed;
  color: rgb(7, 28, 255);
  width: 100%;
}
</style>
