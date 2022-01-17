<template>
  <div class="w-full">
    <!-- hero section -->
    <section class="cover-gradient w-full pb-24">
      <div class="relative max-w-screen-xl px-8 mx-auto grid grid-cols-12 gap-x-6">
        <div class="col-span-12 lg:col-span-6 mt-12 xl:mt-20 space-y-6 px-4">
          <span class="text-base text-gradient font-semibold uppercase">Sign Up Today</span>
          <h1 class="text-5xl xl:text-6xl text-neutral-800 font-bold capitalize sm:pr-8 xl:pr-12">
            The World's <span class="text-header-gradient">Fastest Growing</span> Crypto Web App
          </h1>
          <p class="text-gray-700">
            Buy and sell 200+ cryptocurrencies with 20+ flat currencies using bank transfers or your credit/debit card.
          </p>
          <div class="flex space-x-4 mt-2">
            <button
              class="px-8 py-4 text-sm text-center bg-gradient-to-r from-[#468ef9] to-[#0c66ee] text-white rounded-full"
            >
              Get Started
            </button>
            <button
              class="px-6 py-4 text-sm text-center bg-inherit text-gradient rounded-full border border-[#0c66ee] flex items-center space-x-1"
            >
              <span>Download App</span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="w-3 h-3 text-[#0c66ee]"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
              </svg>
            </button>
          </div>
        </div>
        <div class="col-span-12 lg:col-span-6">
          <div class="w-full">
            <img :src="require('~/assets/img/hero-image.png')" class="-mt-4" alt="" />
          </div>
        </div>
        <img
          :src="require('~/assets/img/pattern/ellipse-1.png')"
          class="absolute bottom-12 xl:bottom-16 left-4 xl:left-0 w-6"
        />
        <img
          :src="require('~/assets/img/pattern/ellipse-2.png')"
          class="absolute top-4 sm:top-10 right-64 sm:right-96 xl:right-[32rem] w-6"
        />
        <img :src="require('~/assets/img/pattern/ellipse-3.png')" class="absolute bottom-56 right-24 w-6" />
        <img
          :src="require('~/assets/img/pattern/star.png')"
          class="absolute top-28 right-16 lg:right-0 lg:left-[30rem] w-8"
        />
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>
<style scoped>
.text-header-gradient {
  background: rgb(57, 132, 244);
  background: linear-gradient(
    347deg,
    rgba(57, 132, 244, 1) 0%,
    rgba(12, 211, 255, 1) 39%,
    rgba(47, 124, 240, 1) 76%,
    rgba(14, 101, 232, 1) 100%
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
</style>
