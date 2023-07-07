<template>
  <div class="d-flex justify-content-center align-items-center h-100">
    <div
      class="card"
      style="display: flex; justify-content: center; align-items: center"
    >
      <div class="row g-0">
        <div class="col-md-6">
          <div class="card-body">
            <h3
              class="about-heading animate__animated animate__fadeInDown animate__delay-1s 1s"
            >
              About Me
            </h3>
            <p
              class="about-content animate__animated animate__fadeInLeft animate__delay-1s 1s"
            >
              I am Mish-Al Taliep, a 21 year old from Belgravia, Cape Town.
              <br />

              I graduated from high school with little to no knowledge on IT or
              web development. However, I was always facinated with technology.

              <br />

              I joined Life Choices' Coding Academy to pursue an interest and
              potentially make it my profession.

              <br />

              Some of my hobbies are soccer, which is my favorite sport, and
              dancing, which has always been more of a passion to me.
            </p>
          </div>
        </div>
        <div
          class="col-md-6 animate__animated animate__bounceIn animate__delay-1s 1s"
        >
          <img
            src="https://i.postimg.cc/9QSyv4vF/IMG-4594.jpg"
            class="img-fluid"
            alt="me"
            loading="lazy"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.about-heading {
  text-decoration: underline;
  color: #cae9ff;
}
.card {
  background: none;
  border: none;
}

.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 20rem;
  flex-direction: column;
}
.about-content {
  color: #1b4965;
  font-size: 1.3rem;
}
.col-md-6 {
  display: flex;
  justify-content: center;
  align-items: center;
}
img {
  display: flex;
  object-fit: cover;
  width: 25rem;
  height: 25rem;
  margin-bottom: 1rem;
  border: 7px solid #cae9ff;
  border-radius: 61% 39% 65% 35% / 38% 62% 38% 62%;
  background-image: linear-gradient(45deg, #1b4965, #5fa8d3 100%);
  background-position: top -10px center;
  background-blend-mode: multiply;
  animation: morph 8s ease-in-out infinite;
}
@keyframes morph {
  0% {
    border-radius: 43% 57% 30% 70% / 62% 32% 68% 38%;
  }
  50% {
    border-radius: 17% 83% 20% 80% / 63% 22% 78% 37%;
    background-image: linear-gradient(45deg, #62b6cb, #bee9e8 50%, #1b4965 90%);
  }
  75% {
    border-radius: 29% 71% 44% 56% / 49% 50% 50% 51%;
  }
  100% {
    border-radius: 43% 57% 30% 70% / 62% 32% 68% 38%;
  }
}
</style>