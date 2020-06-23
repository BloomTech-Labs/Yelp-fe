<template>
  <div>
    <main>
      <div class="mx-auto sm:py-6 max-w-7xl sm:px-6 lg:px-8">
        <div
          class="border-b-4 border-gray-200 sm:mt-4 sm:bg-white sm:border-4 sm:rounded-lg sm:px-4 sm:py-3"
        >
          <sentiment />
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import Sentiment from '~/components/Sentiment'
export default {
  components: {
    Sentiment,
  },
}
</script>
