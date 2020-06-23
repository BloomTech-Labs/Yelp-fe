<template>
  <div class="px-4 py-6 sm:px-0">
    <h1 class="mb-3 text-3xl font-semibold">
      🚧 📎 Extracting Topics from Reviews 🖇️ 🚧
    </h1>
    <div class="max-w-2xl mb-6 text-sm text-gray-500"></div>
    <textarea
      id="review"
      name="review"
      placeholder="I rarely need to use dry cleaner services but a wrinkled t-shirt was not going to fly for my upcoming conference. I picked one that opened pretty early. Suit in hand, I got there first thing at 7am on a Tuesday. Jane at the cash register was so kind and assured me everything would look great. By Wednesday my clothes were pressed professionally and ready for only $15. I’ll definitely use this place again!"
      class="w-full p-3 bg-white border-4 border-gray-300 rounded-lg appearance-none resize-none sm:border-gray-200 sm:border-dashed h-96 focus:outline-none focus:bg-white"
    ></textarea>
    <div class="flex justify-end mt-4">
      <button
        class="px-5 py-3 text-white bg-blue-400 rounded-full hover:bg-blue-500 focus:outline-none hover:shadow-lg"
      >
        Submit
      </button>
    </div>

    <div class="flex max-w-4xl">
      <div class="flex-grow">
        <h3 class="mt-3 mb-2 text-lg font-semibold text-green-500">
          Positive Topics:
        </h3>
        <ul class="text-gray-500 opacity-25">
          <li>Chicken</li>
        </ul>
      </div>
      <div class="flex-grow">
        <h3 class="mt-3 mb-2 text-lg font-semibold text-red-500">
          Negative Topics:
        </h3>
        <ul class="text-gray-500 opacity-25">
          <li>Service</li>
        </ul>
      </div>
    </div>
  </div>
</template>
