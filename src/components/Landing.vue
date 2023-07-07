<template>
  <div class="res d-flex justify-content-center align-items-center h-100">
    <div class="landing">
      <h1 class="animate__animated animate__fadeInDown animate__delay-1s 1s">
        My name is Mish-Al Taliep
      </h1>
      <p class="animate__animated animate__fadeInDown animate__delay-2s 2s">
        An Aspiring Front-End Developer <br />
        Click below to find out more about me
      </p>
      <div class="animate__animated animate__bounceIn animate__delay-3s 3s">
        <router-link class="abtbtn" to="/about"
          ><button class="abtbtn">Read More</button></router-link
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.abtbtn {
  text-decoration: none;
  color: grey;
  background-color: #bee9e8;
  cursor: pointer;
}
p {
  font-size: x-large;
  color: #1b4965;
}
.abtbtn:hover {
  background-color: grey;
  color: #bee9e8;
  border: 1px solid #1b4965;
}
h1 {
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 30px;
}
p {
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 30px;
}
.abtbtn {
  background-color: #bee9e8;
  border: #bee9e8;
  border-radius: 5px;
  height: 3rem;
}
.landing {
  height: 61vh;
  border-radius: 5px;
  color: #cae9ff;
}
.res {
  margin: auto;
}
</style>