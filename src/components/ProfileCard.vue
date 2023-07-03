<template>
    <div>
        <div class="row my-3"></div>
        <h1>Testimonials</h1>
    </div>
    <br>
    <div class="container">
        <div class="row justify-content-center gap-5">
            <div class="card" v-for="humans in testimonials" style="width: 20rem;" :key="humans.id">
            <img :src="humans.image" id="img" class="card-img-top" :alt="humans.name" loading="lazy">
            <div class="card-body">
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
</template>

<script>
    export default {
        computed: {
            testimonials() {
                return this.$store.state.testimonials
            }
        },
        mounted() {
            this.$store.dispatch('fetchTestimonials')
        }
    }
</script>

<style scoped>
#img{
    height: min-content;
    border-radius: 20px;
    margin-top: 1rem;
}

.card-head{
    color: #62B6CB;
}
.card-text{
    color: #5FA8D3;
}
.card{
    background-color: #1B4965;
    border-radius: 20px;
    margin-bottom: 1rem;
}

</style>