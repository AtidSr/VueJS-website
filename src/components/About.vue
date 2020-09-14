<template>
  <section class="section" id="about">
    <div class="row">
      <h2>{{ title }}</h2>
    </div>
    <div class="f info">
      <div class="margin-a">
        <p class="pa w5">{{ text }}</p>
      </div>
      <div class="f margin-a lh-big padding-normal">
        <div class="icon" @mouseover="hovered = true" @mouseleave="hovered = false">
          <img class="Freepik" src="../assets/resume.svg" alt="Freepik icon" />
          <div class="credit" v-if="hovered">
            Icons made by
            <a href="http://www.freepik.com/" title="Freepik">Freepik</a> from
            <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a>
          </div>
        </div>
        <div class="detail">
          <ul>
            <li>
              <h4>Details</h4>
            </li>
            <li>
              Name :
              <span>{{ name }}</span>
            </li>
            <li>
              Age :
              <span>{{ age }}</span>
            </li>
            <li>
              Location :
              <span>{{ location }}</span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data: function () {
    return {
      hovered: false,
      name: "Atid Srisukhantapuek",
      age: "24",
      location: "Bangkok, Thailand",
      title: "About me",
      text:
        "I'm novice front-end developer whom have high interest in technology. I like flat style website also beautiful website. I also like to work as team.",
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.section {
  background-color: #ffffff;
  padding: 5rem;
}
.f {
  display: flex;
  column-gap: 2rem;
}

span {
  font-weight: 100;
  padding-left: 0.5rem;
}

li {
  list-style: none;
}

.credit {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  font-weight: 100;
  font-size: 80%;
  animation: fadeIn 0.3s ease-in;
}

.credit a {
  text-decoration: none;
}
.w5 {
  width: 30vw;
}

.margin-a {
  margin: auto;
}

.padding-normal {
  padding: 2rem 0;
}

.lh-big {
  line-height: 150%;
}

.info {
  justify-content: center;
  flex-direction: column;
  width: 80%;
  margin: auto;
}

.icon {
  text-align: center;
  margin-left: 1rem;
  position: relative;
  display: inline-block;
}

.Freepik {
  display: inline-block;
  width: 8rem;
}

#about {
  font-weight: 300;
  color: #000000;
}

.pa {
  font-size: 90%;
  padding: 1rem 0;
  text-indent: 3rem;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@media only screen and (max-width: 1200px) {
  .w5 {
    width: 40vw;
  }
}

@media only screen and (max-width: 1024px) {
  .w5 {
    width: 50vw;
  }
}
@media only screen and (max-width: 786px) {
  .w5 {
    width: 60vw;
  }
}
@media only screen and (max-width: 480px) {
  .w5 {
    width: 70vw;
  }
  .Freepik {
    width: 5rem;
  }
  .section {
    padding: 2rem;
  }
}
</style>
