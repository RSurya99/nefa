<template>
  <div class="min-h-screen font-sans antialiased relative">
    <div class="relative">
      <div class="absolute top-0 left-0 w-full h-[125vh] cover-gradient"></div>
      <nav class="relative z-10 w-full text-neutral-800">
        <div class="flex flex-col max-w-screen-xl px-8 mx-auto lg:items-center lg:justify-between lg:flex-row py-4">
          <div class="flex flex-col lg:flex-row items-center space-x-4 xl:space-x-8">
            <div class="w-full flex flex-row items-center justify-between py-6">
              <div>
                <img :src="require('~/assets/img/logo/nefa.svg')" class="w-24 xl:w-28" alt="Nefa Logo" />
              </div>
              <button class="rounded-lg lg:hidden focus:outline-none focus:shadow-outline" @click="open = !open">
                <svg fill="currentColor" viewBox="0 0 20 20" class="w-6 h-6">
                  <path
                    v-if="!open"
                    fill-rule="evenodd"
                    d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM9 15a1 1 0 011-1h6a1 1 0 110 2h-6a1 1 0 01-1-1z"
                    clip-rule="evenodd"
                  ></path>
                  <path
                    v-if="open"
                    fill-rule="evenodd"
                    d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
                    clip-rule="evenodd"
                  ></path>
                </svg>
              </button>
            </div>
            <ul
              :class="[open ? 'flex' : 'hidden lg:flex']"
              class="w-full h-auto flex flex-col flex-grow lg:items-center pb-4 lg:pb-0 lg:justify-end lg:flex-row origin-top duration-300 xl:space-x-2 space-y-3 lg:space-y-0"
            >
              <NavLink name="Cryptocurrency" url="#" />
              <NavLink name="Exchanges" url="#" />
              <NavLink name="Watchlist" url="#" />
              <NavLink name="NFT" url="#" />
              <NavLink name="Portfolio" url="#" />
              <li>
                <a
                  class="md:px-4 py-2 text-sm bg-transparent rounded-lg hover:text-gray-900 focus:outline-none focus:shadow-outline flex items-center space-x-1"
                  href="#"
                >
                  <span>Products</span>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="w-3 h-3"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                  >
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
                  </svg>
                </a>
              </li>
            </ul>
          </div>
          <div :class="[open ? 'flex' : 'hidden lg:flex']" class="space-x-3">
            <a
              class="px-8 xl:px-10 py-3 mt-2 text-sm text-center bg-inherit text-gradient rounded-full border border-[#0c66ee]"
              href="#"
              >Login</a
            >
            <a
              class="px-8 xl:px-10 py-3 mt-2 text-sm text-center bg-gradient-to-r from-[#468ef9] to-[#0c66ee] text-white rounded-full"
              href="#"
              >Sign Up</a
            >
          </div>
        </div>
      </nav>

      <main>
        <Nuxt />
      </main>

      <footer class="max-w-screen-xl px-8 mx-auto">
        <div class="w-full border-y border-[#DDDDDD]">
          <div class="w-full flex flex-wrap">
            <div class="w-full sm:w-1/2 xl:w-fit flex sm:px-6 py-12 space-x-10 sm:border-r border-[#DDDDDD]">
              <div class="hidden xl:block">
                <img :src="require('~/assets/img/logo/nefa.svg')" class="w-24 -mt-2" alt="Nefa Logo" />
              </div>
              <ul class="space-y-4">
                <NavLink name="Cryptocurrency" url="#" />
                <NavLink name="Exchanges" url="#" />
                <NavLink name="Watchlist" url="#" />
                <NavLink name="Portfolio" url="#" />
                <NavLink name="NFT" url="#" />
              </ul>
            </div>
            <div class="w-full sm:w-1/2 xl:w-fit px-10 sm:px-16 py-12 xl:border-r border-[#DDDDDD]">
              <ul class="space-y-4">
                <NavLink name="Products" url="#" />
                <NavLink name="About Us" url="#" />
                <NavLink name="Careers" url="#" />
                <NavLink name="Blog" url="#" />
                <NavLink name="Security" url="#" />
              </ul>
            </div>
            <div class="w-full sm:w-1/2 xl:w-fit px-10 sm:px-16 py-12 sm:border-r border-[#DDDDDD]">
              <ul class="space-y-4">
                <NavLink name="Help Center" url="#" />
                <NavLink name="Contact Us" url="#" />
                <NavLink name="System Status" url="#" />
                <NavLink name="Area of Avaibility" url="#" />
                <NavLink name="Privacy Policy" url="#" />
              </ul>
            </div>
            <div class="px-10 py-12 w-full sm:w-1/2 xl:w-[22rem] space-y-4">
              <h5 class="text-sm text-[#666666] hover:text-gray-900 focus:outline-none focus:shadow-outline">
                Newsletter
              </h5>
              <p class="text-sm text-[#666666] hover:text-gray-900 focus:outline-none focus:shadow-outline">
                Never miss anything crypto when you're on the go
              </p>
              <div class="flex items-center space-x-2">
                <input
                  type="text"
                  class="w-full px-2 py-3 rounded-md text-sm focus:outline-none border border-[#AAAAAA] placeholder-[#888]"
                  placeholder="Enter your email"
                />
                <button class="bg-blue-gradient px-4 py-3 rounded-md text-white">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="h-5 w-5"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                      d="M14 5l7 7m0 0l-7 7m7-7H3"
                    />
                  </svg>
                </button>
              </div>
            </div>
          </div>
        </div>
        <div class="py-4 text-center text-sm text-[#666666] hover:text-gray-900">
          &copy; Copyright 2022 NEFA LLC. All rights reserved
        </div>
      </footer>
    </div>
  </div>
</template>
<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      open: false,
    }
  },
}
</script>

<style>
.cover-gradient {
  background: linear-gradient(
    169.4deg,
    rgba(57, 132, 244, 0.04) -6.01%,
    rgba(12, 211, 255, 0.04) 36.87%,
    rgba(47, 124, 240, 0.04) 78.04%,
    rgba(14, 101, 232, 0.04) 103.77%
  );
}
.bg-blue-gradient,
.text-gradient {
  background: linear-gradient(136.91deg, #468ef9 -12.5%, #0c66ee 107.5%);
}
.text-gradient {
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
</style>
