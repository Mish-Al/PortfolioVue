<template>
  <div class="proj">
    <div class="project-head">
      <h1>Projects</h1>
    </div>
    <div
      class="container animate__animated animate__backInDown animate__delay-1s 1s"
    >
      <div class="row justify-content-center gap-5">
        <div
          class="card"
          v-for="ideas in projects"
          style="width: 20rem"
          :key="ideas.id"
        >
          <div class="card-body">
            <h4 class="card-head">
              {{ ideas.name }}
            </h4>
            <a :href="ideas.link" class="pro-btn"><button>Github</button></a>
            <a :href="ideas.website" class="pro-btn"
              ><button>Live Server</button></a
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  computed: {
    projects() {
      return this.$store.state.projects;
    },
  },
  mounted() {
    this.$store.dispatch("fetchProjects");
  },
};
</script>

<style scoped>
.project-head {
  text-decoration: underline;
  color: #cae9ff;
  padding-bottom: 1rem;
}
.proj {
  margin-top: 1rem;
  margin-bottom: 2rem;
}

/* .row {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
} */
.card {
  display: flex;
  justify-content: center;
  background-color: #1b4965;
  border-radius: 20px;
  margin-bottom: 1rem;
  box-shadow: 0 6px 10px rgba(119, 34, 34, 0.08), 0 0 6px rgba(0, 0, 0, 0.05);
  transition: 0.3s transform cubic-bezier(0.155, 1.105, 0.295, 1.12),
    0.3s box-shadow,
    0.3s -webkit-transform cubic-bezier(0.155, 1.105, 0.295, 1.12);
  cursor: pointer;
}
button {
  text-decoration: none;
  color: grey;
  background-color: #bee9e8;
  border: #bee9e8;
  border-radius: 5px;
  height: 3rem;
  margin: 1rem;
}
button:hover {
  background-color: #62b6cb;
  color: #1b4965;
  border: 1px solid #bee9e8;
}
.card:hover {
  transform: scale(1.05);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.12), 0 4px 8px rgba(0, 0, 0, 0.06);
}
.card-head {
  color: #62b6cb;
}
</style>