<template>
  <div class="home">
    <Landing/>
  </div>
</template>

<script>

import Navbar from '@/components/Navbar.vue'
import Landing from '@/components/Landing.vue'

export default {
  name: 'HomeView',
  components: {
    Landing
    
  }
}
</script>
