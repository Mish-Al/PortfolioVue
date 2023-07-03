<template>
  <div>
<nav id="navb" class="navbar navbar-expand">
<div class="container-fluid">
  <a class="navbar-brand" href="#">
      <img
       src="https://i.postimg.cc/8cM31QCS/Screenshot-2023-07-01-122816.png" 
       id="logo"> 
  </a>
  <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="nav-links">
    <ul class="navbar-nav">
      <li class="nav-item">
        <router-link class="nav-link" to="/">Home</router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" to="/about">About</router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" to="/projects">Projects</router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" to="/admin">Resume</router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" to="/testimonials">Testimonials</router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" to="/contact">Contact</router-link>
      </li>
    </ul>
  </div>
</div>
</nav>
  </div>
</template>

<script>
  export default {
      
  }
</script>

<style scoped>
.navbar{
  background-color: #ddf1f4;
  border: 2px solid #1b4965;
  border-radius: 5px;
}
#logo{
  height: 6rem;
  background-color: #cae9ff;
}
#nav-links{
  display: flex;
  justify-content: end;
  text-align: center;
}

.nav-link {
  color: grey;
}
.nav-link:hover{
  color: #5fa8d3;
}

li{
  color: #1b4965;
}



</style>