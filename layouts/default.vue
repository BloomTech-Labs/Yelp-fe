<template>
  <div class="min-h-screen bg-gray-100">
    <navbar />
    <nuxt />
  </div>
</template>

<script>
import Navbar from '~/components/Navbar.vue'

export default {
  components: {
    Navbar,
  },
}
</script>
