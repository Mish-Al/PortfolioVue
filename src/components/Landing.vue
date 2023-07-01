<template>
    <div class="landing">
        <h1>My name is Mish-Al Taliep</h1>
        <p>Welcome To My Personal Portfolio
          <br> Click the button below to find out more about me
        </p>
        <button id="abtbtn">
            <router-link class="abtbtn" to="/about">Read More</router-link>
        </button>
      </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.abtbtn{
    text-decoration: none;
    color: grey;
    background-color: #bee9e8;
}
h1{
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 30px
}
p{
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 30px;
}
#abtbtn{
    background-color: #bee9e8;
    border: #bee9e8;
    border-radius: 5px;
    height: 3rem;
}
.landing{
    background-image: url(https://i.postimg.cc/8cgMx886/Untitled-design.png);
    background-size: cover;
    background-repeat: no-repeat;
    height: 64vh;
    border-radius: 5px;
    color: #cae9ff;
}


</style>