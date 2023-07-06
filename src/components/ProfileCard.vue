<template>
  <div>
    <div class="test-head">
      <h1>Testimonials</h1>
    </div>
    <br />
    <div
      class="container animate__animated animate__bounceIn animate__delay-1s 1s"
    >
      <div class="row justify-content-center gap-5">
        <div
          class="card"
          v-for="humans in testimonials"
          style="width: 20rem"
          :key="humans.id"
        >
          <div class="profile">
            <img
              :src="humans.image"
              id="img"
              class="card-img-top"
              :alt="humans.name"
              loading="lazy"
            />
          </div>
          <div class="card-body p-4">
            <h4 class="card-head">
              {{ humans.name }}
            </h4>
            <p class="card-text">
              {{ humans.comments }}
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
    testimonials() {
      return this.$store.state.testimonials;
    },
  },
  mounted() {
    this.$store.dispatch("fetchTestimonials");
  },
};
</script>

<style scoped>
#img {
  /* height: 290px; */
  border-radius: 20px;
  margin-top: 1rem;
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
.profile {
  width: 100%;
  height: 25rem;
}

.profile img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.profile img {
  width: 100%;
  height: 100%;
}
.test-head {
  text-decoration: underline;
  color: #cae9ff;
}
</style>