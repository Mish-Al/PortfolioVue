<template>
  <div>
    <br />
    <div class="section-heading">
      <h2>Education</h2>
    </div>
    <br />
    <div class="container">
      <div class="row justify-content-center gap-2">
        <div
          class="card"
          v-for="learn in education"
          style="width: 15rem"
          :key="learn.id"
        >
          <div class="card-body">
            <h4 class="card-head">
              {{ learn.place }}
            </h4>
            <img
              :src="learn.imageUrl"
              id="img"
              class="card-img-top"
              :alt="learn.place"
              loading="lazy"
            />
            <p class="card-text">
              {{ learn.type }}
            </p>
            <p class="card-text">
              {{ learn.qualification }}
            </p>
            <p class="card-text">
              {{ learn.duration }}
            </p>
          </div>
        </div>
      </div>
    </div>
    <br />
    <div class="section-heading">
      <h2>Skills</h2>
    </div>
    <br />
    <div class="container">
      <div class="row justify-content-center gap-2">
        <div
          class="card"
          v-for="forte in skills"
          style="width: 15rem"
          :key="forte.id"
        >
          <div class="card-body">
            <h4 class="card-head">
              {{ forte.name }}
            </h4>
            <!-- icon -->
            <i id="icons" style="font-size: 5rem" :class="forte.icon"></i>
            <!--  -->
            <p class="card-text">
              {{ forte.level }}
            </p>
          </div>
        </div>
      </div>
    </div>
    <br />
    <div class="section-heading">
      <h2>Work Experience</h2>
    </div>
    <br />
    <div class="container">
      <div class="row justify-content-center gap-2">
        <div
          class="card"
          v-for="record in experience"
          style="width: 15rem"
          :key="record.id"
        >
          <div class="card-body">
            <h4 class="card-head">
              {{ record.place }}
            </h4>
            <p class="card-text">
              {{ record.type }}
            </p>
            <p class="card-text">
              {{ record.duration }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    education() {
      return this.$store.state.education;
    },
    skills() {
      return this.$store.state.skills;
    },
    experience() {
      return this.$store.state.experience;
    },
  },
  mounted() {
    this.$store.dispatch("fetchEducation");
    this.$store.dispatch("fetchSkills");
    this.$store.dispatch("fetchExperience");
  },
};
</script>

<style scoped>
.container {
  width: 100% !important;
}
.card-head {
  color: #62b6cb;
}
.card-text {
  color: #5fa8d3;
}
.card {
  background-color: #1b4965;
  border-radius: 20px;
  margin-bottom: 1rem;
  box-shadow: 0 6px 10px rgba(119, 34, 34, 0.08), 0 0 6px rgba(0, 0, 0, 0.05);
  transition: 0.3s transform cubic-bezier(0.155, 1.105, 0.295, 1.12),
    0.3s box-shadow,
    0.3s -webkit-transform cubic-bezier(0.155, 1.105, 0.295, 1.12);
  cursor: pointer;
}
.card:hover {
  transform: scale(1.05);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.12), 0 4px 8px rgba(0, 0, 0, 0.06);
}
#icons {
  color: #ddf1f4;
}
#img{
    height: 5rem;
    width: 5rem;
}
.section-heading{
    text-decoration: underline;
    color: #cae9ff;
}
</style>