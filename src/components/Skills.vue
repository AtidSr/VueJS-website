<template>
  <section class="section" id="skill">
    <video autoplay muted loop class="bgVideo">
      <source src="../assets/video/coding.mp4" type="video/mp4" />
    </video>
    <div class="content">
      <div class="row top">
        <h2>{{title}}</h2>
      </div>
      <div class="row">
        <div v-for="(list, index) in lists" :key="list.i" :class="'square-box pic-'+ index">
          <div class="text">{{list.i}}</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data: function () {
    return {
      title: "What can i do?",
      lists: [
        {
          i:
            "I can help developing website (Front-end) that  the requirement of customer",
        },
        {
          i:
            "I can develop java application because java is primary language in my university",
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.section {
  position: relative;
  width: 100vw;
  height: 100vh;
}

.bgVideo {
  object-fit: cover;
  position: fixed;
  width: 100vw;
  height: 100vh;
  bottom: 0%;
  z-index: -2;
}

.top {
  padding-top: 5rem;
}

.content {
  width: 100vw;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.7);
  position: absolute;
  z-index: 2;
  top: 0;
}

.square-box {
  background-color: #fff;
  text-indent: 3rem;
  padding-left: 3rem;
  padding: 3rem;
  margin-bottom: 3rem;
}

.flex {
  display: flex;
}

.pic-0 {
  background-image: linear-gradient(
      105deg,
      #44bd32 0%,
      #44bd32 60%,
      transparent 60%
    ),
    url("../assets/code.jpg");
  background-size: cover;
  background-position: center;
}

.pic-1 {
  background-image: linear-gradient(
      105deg,
      #44bd32 0%,
      #44bd32 60%,
      transparent 60%
    ),
    url("../assets/board.jpg");
  background-size: cover;
  background-position: center;
}

.text {
  width: 60%;
}
</style>
