<template>
  <div>
    <nav class="bg-red-700 shadow-lg">
      <div class="px-4 mx-auto max-w-7xl sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-12 sm:h-16">
          <div class="flex items-center">
            <div class="hidden md:block">
              <div class="flex items-baseline">
                <nuxt-link
                  to="/"
                  class="px-3 py-2 ml-4 text-sm font-medium text-red-200 transition-all duration-200 ease-in-out rounded-md hover:text-white hover:bg-red-600 focus:outline-none"
                  >Home</nuxt-link
                >
                <nuxt-link
                  to="/NLP"
                  class="px-3 py-2 ml-4 text-sm font-medium text-red-200 transition-all duration-200 ease-in-out rounded-md hover:text-white hover:bg-red-600 focus:outline-none"
                  >NLP</nuxt-link
                >
                <nuxt-link
                  to="/recommender"
                  class="px-3 py-2 ml-4 text-sm font-medium text-red-200 transition-all duration-200 ease-in-out rounded-md hover:text-white hover:bg-red-600 focus:outline-none"
                  >Recommender</nuxt-link
                >
                <nuxt-link
                  to="/captioning"
                  class="px-3 py-2 ml-4 text-sm font-medium text-red-200 transition-all duration-200 ease-in-out rounded-md hover:text-white hover:bg-red-600 focus:outline-none"
                  >Photo Captioning</nuxt-link
                >
                <nuxt-link
                  to="/team"
                  class="px-3 py-2 ml-4 text-sm font-medium text-red-200 transition-all duration-200 ease-in-out rounded-md hover:text-white hover:bg-red-600 focus:outline-none"
                  >Team</nuxt-link
                >
                <nuxt-link
                  to="/reports"
                  class="px-3 py-2 ml-4 text-sm font-medium text-red-200 transition-all duration-200 ease-in-out rounded-md hover:text-white hover:bg-red-600 focus:outline-none"
                  >Reports</nuxt-link
                >
              </div>
            </div>
          </div>
          <div class="flex -mr-2 md:hidden">
            <!-- Mobile menu button -->
            <button
              class="inline-flex items-center justify-center p-2 text-right text-red-200 rounded-md hover:text-white hover:bg-red-700 focus:outline-none"
              @click.prevent="menuOpen = !menuOpen"
            >
              <!-- Menu open: "hidden", Menu closed: "block" -->
              <svg
                :class="[menuOpen ? 'hidden' : 'block']"
                class="block w-6 h-6"
                stroke="currentColor"
                fill="none"
                viewBox="0 0 24 24"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 6h16M4 12h16M4 18h16"
                />
              </svg>
              <!-- Menu open: "block", Menu closed: "hidden" -->
              <svg
                :class="[menuOpen ? 'block' : 'hidden']"
                class="w-6 h-6"
                stroke="currentColor"
                fill="none"
                viewBox="0 0 24 24"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M6 18L18 6M6 6l12 12"
                />
              </svg>
            </button>
          </div>
        </div>
      </div>

      <!--
      Mobile menu, toggle classes based on menu state.

      Open: "block", closed: "hidden"
      -->
      <div :class="[menuOpen ? 'block' : 'hidden']" class="md:hidden">
        <div class="px-2 pt-2 pb-3 text-right sm:px-3">
          <nuxt-link
            to="/"
            class="block px-3 py-2 mt-1 text-base font-medium text-red-200 transition-all duration-200 ease-in-out rounded-md hover:text-white hover:bg-red-600 focus:outline-none focus:text-white focus:bg-red-900"
            >Home</nuxt-link
          >
          <nuxt-link
            to="/NLP"
            class="block px-3 py-2 mt-1 text-base font-medium text-red-200 transition-all duration-200 ease-in-out rounded-md hover:text-white hover:bg-red-600 focus:outline-none focus:text-white focus:bg-red-900"
            >NLP</nuxt-link
          >
          <nuxt-link
            to="/recommender"
            class="block px-3 py-2 mt-1 text-base font-medium text-red-200 transition-all duration-200 ease-in-out rounded-md hover:text-white hover:bg-red-600 focus:outline-none focus:text-white focus:bg-red-900"
            >Recommender</nuxt-link
          >
          <nuxt-link
            to="/captioning"
            class="block px-3 py-2 mt-1 text-base font-medium text-red-200 transition-all duration-200 ease-in-out rounded-md hover:text-white hover:bg-red-600 focus:outline-none focus:text-white focus:bg-red-900"
            >Photo Captioning</nuxt-link
          >
          <nuxt-link
            to="/team"
            class="block px-3 py-2 mt-1 text-base font-medium text-red-200 transition-all duration-200 ease-in-out rounded-md hover:text-white hover:bg-red-600 focus:outline-none focus:text-white focus:bg-red-900"
            >Team</nuxt-link
          >
          <nuxt-link
            to="/reports"
            class="block px-3 py-2 mt-1 text-base font-medium text-red-200 transition-all duration-200 ease-in-out rounded-md hover:text-white hover:bg-red-600 focus:outline-none focus:text-white focus:bg-red-900"
            >Reports</nuxt-link
          >
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menuOpen: false,
    }
  },
  watch: {
    $route(to, from) {
      this.menuOpen = false
    },
  },
}
</script>

<style lang="postcss" scoped>
.nuxt-link-exact-active {
  @apply bg-red-800 text-white;
}
</style>
