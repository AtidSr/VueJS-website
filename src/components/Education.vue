<template>
  <section class="section" id="edu">
    <div class="row">
      <h2>{{ title }}</h2>
    </div>
    <div class="row info">
      <div class="column">
        <img src="../assets/KU_Logo.png" alt="kasetart university logo" />
      </div>
      <div class="column-1">
        <div class="y">{{ duration }}</div>
      </div>
      <div class="column-2">
        <p class="c">{{ university }}</p>
        <p class="subPa">{{ department }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data: function () {
    return {
      title: "Education",
      duration: "2015 - 2019",
      university: "Kasetsart University",
      department: "Software & Knowledge Engineering",
      name: "wikipedia.org",
      comment:
        "Kasetsart University (KU) is a public research university in Bangkok, Thailand. It was Thailand's first agricultural university and Thailand's third oldest university. Kasetsart University has expanded its subject areas to cover life sciences, science, engineering, social sciences, and humanities. Kasetsart University's main campus is in Bangkhen, northern Bangkok, with several other campuses throughout Thailand. It is one of the largest university in Thailand.",
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.c {
  font-size: 140%;
  text-align: left;
}

.column img {
  width: 5rem;
}

.info {
  display: flex;
  justify-content: center;
  width: 90%;
}

.y {
  padding: 1rem 3rem 0 3rem;
}

.subPa {
  font-family: "Nunito", sans-serif;
  font-weight: 200;
  font-size: 80%;
}

.section {
  padding: 6rem 0;
  color: #000000;
  background-color: #ffffff;
}
</style>
