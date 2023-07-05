<template>
    <div class="res">
    <div class="landing">
        <h1>My name is Mish-Al Taliep</h1>
        <p>Welcome To My Personal Portfolio
          <br> Click the button below to find out more about me
        </p>
            <router-link class="abtbtn" to="/about"><button class="abtbtn">Read More</button></router-link>
      </div>
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
.abtbtn{
    background-color: #bee9e8;
    border: #bee9e8;
    border-radius: 5px;
    height: 3rem;
}
.landing{
    height: 61vh;
    border-radius: 5px;
    color: #cae9ff;
}
.res{
    margin-top: 2rem;
    margin-bottom: 2rem;
}


</style>