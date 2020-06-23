<template>
  <div class="px-4 py-6 sm:px-0">
    <h1 class="mb-3 text-3xl font-semibold">
      NLP
    </h1>
    <!-- <div class="flex flex-row items-center max-w-md m-3 text-2xl">
      <div
        :class="{ 'opacity-25': sentiment === false }"
        class="flex flex-row items-center w-full transition-all duration-500"
      >
        <div>
          😠
        </div>
        <div class="flex items-center flex-grow h-2 mx-3 rounded-lg slider">
          <div
            ref="indicator"
            class="w-4 h-4 transition-all duration-500 bg-white border border-gray-700 rounded-full opacity-85"
            style="margin-left: 50%;"
          ></div>
        </div>
        <div>
          😄
        </div>
      </div>
    </div> -->
    <form class="mb-6" @submit.prevent="submit">
      <div class="mt-6 max-w-sm">
        <label
          for="model_type"
          class="block text-sm leading-5 font-bold text-gray-700"
          >Model Type:
        </label>
        <select
          id="model_type"
          v-model="model_type"
          class="mt-1 form-select block w-full pl-3 pr-10 py-2 text-base leading-6 border-gray-300 focus:outline-none focus:shadow-outline-blue focus:border-blue-300 sm:text-sm sm:leading-5"
          @change="changeModelType"
        >
          <option value="sentiment" selected>Sentiment Analysis </option>
          <option value="summarization">Summarization </option>
        </select>
        <div
          v-show="model_type === 'summarization'"
          class="text-sm text-gray-500 font-bold mt-2"
        >
          This model may take ~30 seconds.
        </div>
      </div>
      <div v-if="model_type == 'sentiment'" class="mt-4 max-w-sm">
        <label
          for="model_name"
          class="block text-sm leading-5 font-bold text-gray-700"
          >Model Name:
        </label>
        <select
          id="model_name"
          v-model="model_name"
          class="mt-1 form-select block w-full pl-3 pr-10 py-2 text-base leading-6 border-gray-300 focus:outline-none focus:shadow-outline-blue focus:border-blue-300 sm:text-sm sm:leading-5"
          @change="changeModelName"
        >
          <option value="distilbert-regression" selected>Regression </option>
          <option value="default">Classification </option>
        </select>
      </div>
      <div v-if="model_type == 'summarization'" class="mt-4 max-w-sm">
        <label
          for="model_name"
          class="block text-sm leading-5 font-bold text-gray-700"
          >Model Name:
        </label>
        <select
          id="model_name"
          v-model="model_name"
          class="mt-1 form-select block w-full pl-3 pr-10 py-2 text-base leading-6 border-gray-300 focus:outline-none focus:shadow-outline-blue focus:border-blue-300 sm:text-sm sm:leading-5"
          @change="changeModelName"
        >
          <option value="bart" selected>BART </option>
          <option value="t5">T5 </option>
        </select>
      </div>
      <div class="mt-4">
        <label
          for="review"
          class="block text-sm leading-5 font-bold text-gray-700"
          >Review:
        </label>
        <textarea
          id="review"
          v-model="review"
          name="review"
          placeholder="The definition of a hole-in-the-wall. I got the regular hamburger and wow…  there are no words. A classic burger done right. Crisp bun, juicy patty, stuffed with all the essentials (ketchup, shredded lettuce, tomato, and pickles). There’s about a million options available between the menu board and wall full of specials, so it can get a little overwhelming, but you really can’t go wrong. Not much else to say besides go see for yourself! You won’t be disappointed."
          class="w-full mt-1 p-3 bg-white border-4 border-gray-300 rounded-lg appearance-none resize-none sm:border-gray-200 sm:border-dashed h-96 focus:outline-none"
        ></textarea>
      </div>
      <div class="flex justify-end mt-4">
        <button
          :disabled="loading"
          class="px-5 py-3 text-white bg-blue-400 rounded-full disabled:opacity-25 hover:bg-blue-500 hover:shadow-lg"
        >
          Submit
        </button>
      </div>
    </form>
    <div v-show="result">
      <hr />
      <div class="mt-6">
        <h2 class="mb-3 text-xl font-semibold">
          Result:
        </h2>
        <div v-if="model_type === 'summarization'">
          {{ result.summary_text }}
        </div>

        <div
          v-if="model_name === 'default'"
          :style="{ opacity: result.score }"
          class="text-5xl"
        >
          <template v-if="result.label === 'POSITIVE'">
            👍
          </template>
          <template v-else-if="result.label === 'NEGATIVE'">
            👎
          </template>
          <template v-else>
            🤷‍♂️
          </template>
        </div>

        <div
          v-show="model_name === 'distilbert-regression'"
          class="flex flex-row items-center max-w-md m-3 text-2xl"
        >
          <div
            class="flex flex-row items-center w-full transition-all duration-500"
          >
            <div>
              😠
            </div>
            <div class="flex items-center flex-grow h-2 mx-3 rounded-lg slider">
              <div
                ref="indicator"
                class="w-4 h-4 transition-all duration-500 bg-white border border-gray-700 rounded-full opacity-85"
                style="margin-left: 50%;"
              ></div>
            </div>
            <div>
              😄
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      review: '',
      loading: false,
      result: false,
      model_type: 'sentiment',
      model_name: 'distilbert-regression',
    }
  },
  methods: {
    changeModelType() {
      this.result = false
      if (this.model_type === 'sentiment') {
        this.model_name = 'distilbert-regression'
      } else if (this.model_type === 'summarization') {
        this.model_name = 'bart'
      }
    },
    changeModelName() {
      this.result = false
    },
    async submit(e) {
      this.loading = true
      const data = {
        text: this.review,
        model_name: this.model_name,
      }
      const res = await this.$axios.$post(
        `https://8rq6v9dni0.execute-api.us-east-1.amazonaws.com/dev/${this.model_type}`,
        data
      )
      this.loading = false
      this.result = res
      if (this.model_name === 'distilbert-regression') {
        this.moveIndicator(res.score)
      }
    },
    moveIndicator(sentiment) {
      const margin = Math.min(sentiment * 100, 96)
      this.$refs.indicator.style.marginLeft = `${margin}%`
      if (this.review.length === 0) {
        this.$refs.indicator.style.marginLeft = '50%'
      }
    },
  },
}
</script>

<style scoped>
.slider {
  background: rgb(236, 98, 98);
  background: linear-gradient(
    90deg,
    rgba(236, 98, 98, 1) 0%,
    rgba(76, 209, 138, 1) 100%
  );
}
</style>
