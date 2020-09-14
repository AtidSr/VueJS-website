<template>
  <header id="home">
    <nav>
      <div class="row clearfix">
        <ul class="main-nav">
          <li v-for="list in lists" :key="list.menu">
            <a :href="'#' + list.id">{{ list.menu }}</a>
          </li>
        </ul>
      </div>
    </nav>

    <div class="text-box" id="content">
      <span class="text-sub">
        <h3>{{ name }} 's</h3>
      </span>
      <span class="text-main">
        <h1>{{ item }}</h1>
      </span>
    </div>
  </header>
</template>

<script>
export default {
  data: function () {
    return {
      name: "Atid Srisukhantapuek",
      item: "Personal site",
      lists: [
        { menu: "home", id: "home" },
        { menu: "about me", id: "about" },
        { menu: "education", id: "edu" },
        { menu: "What ican do?", id: "skill" },
        { menu: "Github" },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header {
  background-image: linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.1)),
    url(../assets/golf-min.jpg);
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  height: 100vh;
}
nav {
  float: right;
}
.text-main {
  font-size: 200%;
  letter-spacing: 0.5rem;
  line-height: 100%;
}

.text-sub {
  padding: 0 0.8rem;
}

.text-box {
  margin: 0;
  padding: 0;
  text-align: right;
  position: absolute;
  top: 47%;
  right: 12%;
  animation: moveIn 0.5s ease-out 0.75s;
  animation-fill-mode: backwards;
}

@keyframes moveIn {
  0% {
    opacity: 0;
    transform: translateY(4rem);
  }

  80% {
    transform: translateY(-1rem);
  }

  100% {
    opacity: 1;
    transform: translate(0);
  }
}

.main-nav {
  margin-top: 3rem;
  margin-right: 3rem;
}

.main-nav li {
  display: inline-block;
  font-size: 90%;
  text-transform: uppercase;
  list-style: none;
  margin: 0 1.5rem;
  transition: all 0.2s;
}

.main-nav li:hover {
  transform: scale(1.1);
}

.main-nav li:hover::after {
  display: block;
  height: 0.15rem;
  background-color: #44bd32;
  content: " ";
  width: inherit;
  margin: 0 auto;
  margin-top: 0.6rem;
  animation: stetchOut 0.4s forwards;
}

.main-nav li a:link,
.main-nav li a:visited {
  text-decoration: none;
  border-bottom: 0.5rem solid transparent;
  padding: 0.7rem 0;

  color: #ffffff;
}

@media only screen and (max-width: 1024px) {
  .text-main {
    font-size: 160%;
    line-height: 150%;
    padding: 0;
  }
}

@media only screen and (max-width: 786px) {
  .main-nav {
    display: none;
  }
}

@media only screen and (max-width: 480px) {
  .text-main {
    font-size: 120%;
  }
  .text-sub {
    font-size: 110%;
  }
}
</style>
