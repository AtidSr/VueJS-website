<template>
  <div id="app">
    <Header />
    <AboutContent />
    <InterestContent />
    <EduContent />
    <Skill />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import AboutContent from "./components/About.vue";
import InterestContent from "./components/Interest.vue";
import EduContent from "./components/Education.vue";
import Skill from "./components/Skills.vue";
import Footer from "./components/footer.vue";

export default {
  name: "App",
  components: {
    Header,
    AboutContent,
    InterestContent,
    EduContent,
    Skill,
    Footer,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Lato:wght@100;300&family=Nunito:ital,wght@0,200;0,300;1,200&display=swap");

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: "Nunito", Avenir, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 125%;
  color: #ffffff;
  text-rendering: optimizeLegibility;
}

.section {
  clear: both;
  padding: 0;
  margin: 0;
}

.row {
  margin: 0 auto;
  max-width: max-content;
}

.clearfix {
  zoom: 1;
}
.clearfix::after {
  content: ".";
  clear: both;
  display: block;
  height: 0;
  visibility: hidden;
}

h2 {
  text-align: center;
  font-size: 180%;
  word-spacing: 0.2rem;
  margin-bottom: 2rem;
  letter-spacing: 0.1rem;
}

h1,
h2,
h3 {
  font-weight: 300;
  text-transform: uppercase;
}

h2:after {
  display: block;
  height: 0.2rem;
  background-color: #44bd32;
  content: " ";
  width: 10rem;
  max-width: 10rem;
  margin: 0 auto;
  margin-top: 1.5rem;
}

h2:hover {
  transform: scale(1.1);
}

h2:hover:after {
  animation: stetchOut 0.5s forwards;
}

p {
  font-family: "Lato", Avenir, Helvetica, sans-serif;
}

@keyframes stetchOut {
  0% {
    width: 0%;
  }

  100% {
    width: 100%;
  }
}

@media only screen and (max-width: 480px) {
  #app {
    font-size: 100%;
  }
}
</style>
