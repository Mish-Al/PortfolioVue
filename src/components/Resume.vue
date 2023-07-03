<template>
    <div>
        <div class="row my-3">
            <h2>Education</h2>
        </div>
        <div class="container">
            <div class="row justify-content-center gap-2">
                <div class="card" v-for="learn in education" style="width: 15rem" :key="learn.id">
                    <div class="card-body">
                        <h4 class="card-head">
                            {{ learn.place }}
                        </h4>
                        <img :src="learn.imageUrl" id="img" class="card-img-top" :alt="learn.place" loading="lazy">
                        <p class="card-text">
                            {{ learn.type }}
                        </p>
                        <p class="card-text">
                            {{ learn.qualification }}
                        </p>
                        <p class="card-text">
                            {{ learn.duration }}
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="row my-3">
            <h2>Skills</h2>
        </div>
        <div class="container">
            <div class="row justify-content-center gap-2">
                <div class="card" v-for="forte in skills" style="width: 15rem" :key="forte.id">
                    <div class="card-body">
                        <h4 class="card-head">
                            {{ forte.name }}
                        </h4>
                        <img :src="forte.icon" id="icon" class="card-img-top" :alt="forte.name" loading="lazy">
                        <p class="card-text">
                            {{ forte.level }}
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="row my-3">
            <h2>Work Experience</h2>
        </div>
        <div class="container">
            <div class="row justify-content-center gap-2">
                <div class="card" v-for="record in experience" style="width: 15rem" :key="record.id">
                    <div class="card-body">
                        <h4 class="card-head">
                            {{ record.place }}
                        </h4>
                        <p class="card-text">
                            {{ record.type }}
                        </p>
                        <p class="card-text">
                            {{ record.duration }}
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
            education() {
                return this.$store.state.education
            },
            skills() {
                return this.$store.state.skills
            },
            experience() {
                return this.$store.state.experience
            }
        },
        mounted() {
            this.$store.dispatch('fetchEducation')
            this.$store.dispatch('fetchSkills')
            this.$store.dispatch('fetchExperience')
        }
    }
</script>

<style scoped>

</style>