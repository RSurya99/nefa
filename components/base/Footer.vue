<template>
  <footer class="max-w-screen-xl px-8 mx-auto">
    <div class="w-full border-y border-[#DDDDDD]">
      <div class="w-full flex flex-wrap">
        <div class="w-full sm:w-1/2 xl:w-fit flex sm:px-6 py-12 space-x-10 sm:border-r border-[#DDDDDD]">
          <div class="hidden xl:block">
            <a href="#">
              <img :src="require('~/assets/img/logo/nefa.svg')" class="w-24 -mt-2" alt="Nefa Logo" />
            </a>
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
          <h5 class="text-sm text-[#666666] focus:outline-none focus:shadow-outline">Newsletter</h5>
          <p class="text-sm text-[#666666] focus:outline-none focus:shadow-outline">
            Never miss anything crypto when you're on the go
          </p>
          <div class="flex items-center space-x-2">
            <input
              type="text"
              class="w-full px-2 py-3 rounded-md text-sm focus:outline-none border border-[#AAAAAA] placeholder-[#888]"
              placeholder="Enter your email"
            />
            <button class="bg-blue-gradient px-4 py-3 rounded-md text-white hover:shadow-md transition duration-300">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-5 w-5"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3" />
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
</template>
<script>
export default {
  name: 'BaseFooter',
}
</script>
