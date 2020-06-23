<template>
  <div class="px-4 py-6 sm:px-0">
    <h1 class="mb-3 text-3xl font-semibold">
      🚧 📸 Extracting Menu from Photo 📷 🚧
    </h1>
    <div class="max-w-2xl mb-6 text-sm text-gray-500"></div>
    <div>
      <button
        class="flex flex-col items-center justify-center w-full p-3 bg-gray-100 border-4 border-gray-200 border-dashed rounded-lg cursor-pointer focus:outline-none h-96"
      >
        <svg
          class="inline-block w-12 h-12 text-gray-300 fill-current"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 20 20"
        >
          <path
            d="M10,8c-1.657,0-3,1.344-3,3c0,1.656,1.343,3,3,3c1.656,0,3-1.344,3-3C13,9.344,11.656,8,10,8z M18,5h-2.4
	c-0.33,0-0.686-0.256-0.789-0.57l-0.621-1.861C14.085,2.256,13.731,2,13.4,2H6.6C6.27,2,5.914,2.256,5.811,2.568L5.189,4.43
	C5.085,4.744,4.73,5,4.4,5H2C0.9,5,0,5.9,0,7v9c0,1.1,0.9,2,2,2h16c1.1,0,2-0.9,2-2V7C20,5.9,19.1,5,18,5z M10,16
	c-2.762,0-5-2.238-5-5c0-2.762,2.238-5,5-5c2.761,0,5,2.238,5,5C15,13.762,12.761,16,10,16z M17.5,8.2c-0.387,0-0.7-0.314-0.7-0.701
	c0-0.385,0.313-0.7,0.7-0.7s0.7,0.314,0.7,0.7C18.2,7.886,17.887,8.2,17.5,8.2z"
          />
        </svg>
        <div class="mt-2 text-gray-400">
          Click to upload photo of a menu
        </div>
      </button>
    </div>
    <div class="py-2 -my-2 overflow-x-auto sm:-mx-6 sm:px-6 lg:-mx-8 lg:px-8">
      <h3 class="mt-3 mb-2 text-lg font-semibold">
        Menu:
      </h3>
      <div
        class="inline-block min-w-full overflow-hidden align-middle border border-gray-200 sm:rounded-lg"
      >
        <table class="min-w-full">
          <thead>
            <tr>
              <th
                class="px-6 py-3 text-xs font-medium leading-4 tracking-wider text-left text-gray-500 uppercase border-b border-gray-200 bg-gray-50"
              >
                Name
              </th>
              <th
                class="px-6 py-3 text-xs font-medium leading-4 tracking-wider text-left text-gray-500 uppercase border-b border-gray-200 bg-gray-50"
              >
                Description
              </th>
              <th
                class="px-6 py-3 text-xs font-medium leading-4 tracking-wider text-left text-gray-500 uppercase border-b border-gray-200 bg-gray-50"
              >
                Additions
              </th>
              <th
                class="px-6 py-3 text-xs font-medium leading-4 tracking-wider text-left text-gray-500 uppercase border-b border-gray-200 bg-gray-50"
              >
                Group
              </th>

              <th
                class="px-6 py-3 text-xs font-medium leading-4 tracking-wider text-left text-gray-500 uppercase border-b border-gray-200 bg-gray-50"
              >
                Cost
              </th>
              <th class="px-6 py-3 border-b border-gray-200 bg-gray-50"></th>
            </tr>
          </thead>
          <tbody class="bg-white opacity-25">
            <tr>
              <td
                class="px-6 py-4 text-sm font-medium leading-5 text-gray-500 border-b border-gray-200"
              >
                CHICKEN SANDWICH
              </td>
              <td
                class="px-6 py-4 text-sm leading-5 text-gray-500 border-b border-gray-200"
              >
                FRIED CHICKEN THIGH OR PULLED SPIT-ROASTED CHICKEN BRIOCHE BUN,
                HERB MAYO, LETTUCE, PICKLES
              </td>
              <td
                class="px-6 py-4 text-sm leading-5 text-gray-500 border-b border-gray-200"
              >
                None
              </td>
              <td
                class="px-6 py-4 text-sm leading-5 text-gray-500 border-b border-gray-200"
              >
                Sandwiches
              </td>

              <td
                class="px-6 py-4 text-sm leading-5 text-gray-500 border-b border-gray-200"
              >
                10
              </td>
              <td
                class="px-6 py-4 text-sm font-medium leading-5 text-right border-b border-gray-200"
              >
                <a href="#" class="text-indigo-500 hover:text-indigo-500"
                  >Edit</a
                >
              </td>
            </tr>
            <tr>
              <td
                class="px-6 py-4 text-sm font-medium leading-5 text-gray-500 border-b border-gray-200"
              >
                CHELSEA’S SHAMELESS PLEA
              </td>
              <td
                class="px-6 py-4 text-sm leading-5 text-gray-500 border-b border-gray-200"
              >
                QUARTER FRIED CHICKEN, BELGIAN WAFFLE, APPLE COMPOTE, WHIPPED
                SORGHUM BUTTER, MAPLE SYRUP. CHOICE OF WHITE OR DARK MEAT.
              </td>
              <td
                class="px-6 py-4 text-sm leading-5 text-gray-500 border-b border-gray-200"
              >
                SORGHUM GLAZED PORK BELLY $3
              </td>
              <td
                class="px-6 py-4 text-sm leading-5 text-gray-500 border-b border-gray-200"
              >
                Entrees
              </td>
              <td
                class="px-6 py-4 text-sm leading-5 text-gray-500 border-b border-gray-200"
              >
                14
              </td>
              <td
                class="px-6 py-4 text-sm font-medium leading-5 text-right border-b border-gray-200"
              >
                <a href="#" class="text-indigo-500 hover:text-indigo-500"
                  >Edit</a
                >
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>
