<template>
  <section class="section" id="inte">
    <div class="row">
      <h2>{{ title }}</h2>
    </div>
    <div class="ls">
      <ul v-for="list in lists" :key="list.item">
        <li>{{ list.item }}</li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  data: function () {
    return {
      title: "Like & interests",
      lists: [
        { item: "Technologies" },
        { item: "Games" },
        { item: "PC" },
        { item: "Manga" },
        { item: "Animation" },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.section {
  width: 100%;
  height: 60vh;
  padding-top: 3.5rem;
  background-image: linear-gradient(
      to right bottom,
      rgba(0, 0, 0, 0.8),
      rgba(0, 0, 0, 0.6)
    ),
    url(../assets/gundam.jpg);
  background-size: cover;
  background-blend-mode: overlay;
  background-attachment: fixed;
}

.ls {
  font-size: 110%;
  width: 40%;
  padding: 1rem 1rem 1rem 3rem;
  margin: auto;
  margin-top: 3.3rem;
}
</style>
