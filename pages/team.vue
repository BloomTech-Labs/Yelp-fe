<template>
  <div>
    <main>
      <div class="py-6 mx-auto max-w-7xl sm:px-6 lg:px-8">
        <div class="text-center">
          <h1 class="text-3xl font-semibold">
            Our Team
          </h1>
          <p>
            We are 3 students from the Lambda School PT Labs 9 cohort.
          </p>
        </div>
        <div
          class="flex flex-wrap justify-center mt-6 border-b-4 border-gray-200 sm:border-none"
        >
          <div
            v-for="user in users"
            :key="user.id"
            class="px-3 py-5 transition-all duration-100 ease-in-out bg-white border-t-4 border-gray-200 sm:my-4 sm:border-4 sm:rounded-lg sm:mx-4 w-96"
          >
            <img
              class="w-48 h-48 mx-auto rounded-full shadow-md"
              :src="user.avatar"
            />

            <h3 class="mt-4 text-2xl font-bold text-center">
              {{ user.name }}
            </h3>

            <div v-if="user.bio" class="text-center">
              {{ user.bio }}
            </div>

            <div
              class="flex flex-col justify-center mt-3 text-sm text-gray-500"
            >
              <a
                v-if="user.linkedin"
                :href="user.linkedin"
                class="flex items-center mx-3 my-2 hover:text-gray-700"
              >
                <svg class="h-5 mr-3" fill="currentColor" viewBox="0 0 20 20">
                  <path
                    d="M5,3c0,1.1-0.7,2-2,2C1.8,5,1,4.1,1,3.1C1,2,1.8,1,3,1S5,1.9,5,3z M1,19h4V6H1V19z M14.6,6.2c-2.1,0-3.3,1.2-3.8,2h-0.1
	l-0.2-1.7H6.9C6.9,7.6,7,8.9,7,10.4V19h4v-7.1c0-0.4,0-0.7,0.1-1c0.3-0.7,0.8-1.6,1.9-1.6c1.4,0,2,1.2,2,2.8V19h4v-7.4
	C19,7.9,17.1,6.2,14.6,6.2z"
                  />
                </svg>
                {{ user.name }}
              </a>
              <a
                :href="user.github"
                class="flex items-center mx-3 my-2 hover:text-gray-700"
              >
                <svg class="h-5 mr-3" fill="currentColor" viewBox="0 0 20 20">
                  <path
                    d="M13.18,11.309c-0.718,0-1.3,0.807-1.3,1.799c0,0.994,0.582,1.801,1.3,1.801s1.3-0.807,1.3-1.801
	C14.479,12.116,13.898,11.309,13.18,11.309z M17.706,6.626c0.149-0.365,0.155-2.439-0.635-4.426c0,0-1.811,0.199-4.551,2.08
	c-0.575-0.16-1.548-0.238-2.519-0.238c-0.973,0-1.945,0.078-2.52,0.238C4.74,2.399,2.929,2.2,2.929,2.2
	C2.14,4.187,2.148,6.261,2.295,6.626C1.367,7.634,0.8,8.845,0.8,10.497c0,7.186,5.963,7.301,7.467,7.301
	c0.342,0,1.018,0.002,1.734,0.002c0.715,0,1.392-0.002,1.732-0.002c1.506,0,7.467-0.115,7.467-7.301
	C19.2,8.845,18.634,7.634,17.706,6.626z M10.028,16.915H9.972c-3.771,0-6.709-0.449-6.709-4.115c0-0.879,0.31-1.693,1.047-2.369
	c1.227-1.127,3.305-0.531,5.662-0.531c0.01,0,0.02,0,0.029,0c0.01,0,0.018,0,0.027,0c2.357,0,4.436-0.596,5.664,0.531
	c0.735,0.676,1.045,1.49,1.045,2.369C16.737,16.466,13.8,16.915,10.028,16.915z M6.821,11.309c-0.718,0-1.3,0.807-1.3,1.799
	c0,0.994,0.582,1.801,1.3,1.801c0.719,0,1.301-0.807,1.301-1.801C8.122,12.116,7.54,11.309,6.821,11.309z"
                  />
                </svg>
                {{ user.githubHandle }}
              </a>
              <a
                v-if="user.website"
                :href="user.website"
                class="flex items-center mx-3 my-2 hover:text-gray-700"
              >
                <svg class="h-5 mr-3" fill="currentColor" viewBox="0 0 24 24">
                  <path
                    d="M4.06 13a8 8 0 0 0 5.18 6.51A18.5 18.5 0 0 1 8.02 13H4.06zm0-2h3.96a18.5 18.5 0 0 1 1.22-6.51A8 8 0 0 0 4.06 11zm15.88 0a8 8 0 0 0-5.18-6.51A18.5 18.5 0 0 1 15.98 11h3.96zm0 2h-3.96a18.5 18.5 0 0 1-1.22 6.51A8 8 0 0 0 19.94 13zm-9.92 0c.16 3.95 1.23 7 1.98 7s1.82-3.05 1.98-7h-3.96zm0-2h3.96c-.16-3.95-1.23-7-1.98-7s-1.82 3.05-1.98 7zM12 22a10 10 0 1 1 0-20 10 10 0 0 1 0 20z"
                  />
                </svg>
                {{ user.website }}
              </a>
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: [
        {
          id: 1,
          name: 'Spencer Adams',
          avatar:
            'https://avatars2.githubusercontent.com/u/2055801?s=460&u=2e8d9831dc72da5d99a127d070f7985a40fcacfb&v=4',
          github: 'https://github.com/spentaur',
          githubHandle: 'spentaur',
          linkedin: 'https://linkedin.com/in/spentaur',
          bio: 'From dishwasher to data scientist.',
          website: 'https://spentaur.com',
        },
        {
          id: 2,
          name: 'Connor Sanderford',
          avatar: '/images/connor.jpg',
          github: 'https://github.com/crsanderford',
          githubHandle: 'crsanderford',
          linkedin: 'https://www.linkedin.com/in/connor-sanderford/',
          website: 'https://crsanderford.github.io/',
          bio: 'Loves math, biology, and the places where they meet.',
        },
        {
          id: 3,
          name: 'Bethany Richardson',
          avatar:
            'https://avatars2.githubusercontent.com/u/51799343?s=460&u=cc7cd70771da267f60437f6551c05cb415f5d1fe&v=4',
          github: 'http://github.com/ravenha',
          githubHandle: 'ravenha',
          linkedin: 'https://www.linkedin.com/in/ravenha',
          website: 'https://ravenha.github.io/',
        },
      ],
    }
  },
  mounted() {
    for (let i = this.users.length - 1; i > 0; i--) {
      const j = Math.floor(Math.random() * i)
      const temp = this.users[i]
      this.users.splice(i, 1, this.users[j])
      this.users.splice(j, 1, temp)
    }
  },
  methods: {
    shuffle(array) {
      const tempArray = new Array(array.length)

      return tempArray
    },
  },
}
</script>
