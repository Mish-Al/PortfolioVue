<template>
  <Navbar />
  <router-view />
  <Footer />
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Footer from "@/components/Footer.vue";
export default {
  components: {
    Navbar,
    Footer,
  },
};
</script>

<style>
#app {
  display: grid;
  grid-template-columns: 100%;
  grid-template-rows: auto minmax(100vh, 1fr);
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
body {
  background-image: url(https://i.postimg.cc/8cgMx886/Untitled-design.png);
  background-size: cover;

  background-repeat: no-repeat;
}

::-webkit-scrollbar {
  display: none;
}
</style>
