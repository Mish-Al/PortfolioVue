<template>
    <div>
        <div class="row my-3"></div>
        <h1>Testimonials</h1>
    </div>
    <div class="container">
        <div class="row justify-content-center gap-5">
            <div class="card p-0" v-for="humans in testimonials" style="width: 15rem;" :key="humans.id">
            <img :src="humans.image" class="card-img-top" :alt="humans.name">
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

</style>