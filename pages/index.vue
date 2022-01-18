<template>
  <div class="w-full">
    <!-- Hero section -->
    <section class="w-full pb-24">
      <div class="relative max-w-screen-xl px-8 mx-auto grid grid-cols-12 gap-x-6">
        <div class="col-span-12 lg:col-span-6 mt-12 xl:mt-20 space-y-6 px-6">
          <span class="text-base text-gradient font-semibold uppercase">Sign Up Today</span>
          <h1 class="text-5xl xl:text-6xl font-bold capitalize sm:pr-8 xl:pr-12">
            The World's <span class="text-header-gradient">Fastest Growing</span> Crypto Web App
          </h1>
          <p class="text-gray-700 tracking-wide leading-relaxed">
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

    <!-- Crypto statistic section -->
    <section
      class="max-w-screen-xl mx-auto px-10 lg:px-0 py-6 sm:py-8 rounded-xl bg-white shadow-md transform lg:-translate-y-12"
    >
      <div class="w-full flex flex-col lg:flex-row items-center justify-center space-y-6 lg:space-y-0 lg:space-x-8">
        <div class="w-1/3 overflow-hidden space-y-6 border-r border-gray-200 px-8">
          <div class="w-full flex items-center justify-between">
            <h3 class="font-medium">🔥 Trending</h3>
            <a href="#" class="text-sm font-medium text-blue-500 flex items-center space-x-1">
              <span>More</span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-3 w-3"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
              </svg>
            </a>
          </div>
          <div class="flex flex-col">
            <div class="-my-2 overflow-x-auto sm:-mx-6 lg:-mx-8">
              <div class="py-2 align-middle inline-block min-w-full px-6 overflow-hidden">
                <table class="min-w-full">
                  <thead>
                    <tr>
                      <th class="text-left text-sm font-medium text-gray-500">Name</th>
                      <th class="text-left text-sm font-medium text-gray-500">Price</th>
                      <th class="text-left text-sm font-medium text-gray-500">Chart</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr v-for="trending in trendings" :key="trending.id" class="border-b border-gray-200">
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center space-x-2">
                          <img :src="require(`~/assets/img/crypto-icon/${trending.logo}`)" alt="" />
                          <span>{{ trending.name }}</span>
                        </div>
                      </td>
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-4 w-4"
                            :class="[trending.increase ? 'text-emerald-500' : 'text-red-500']"
                            viewBox="0 0 20 20"
                            fill="currentColor"
                          >
                            <path
                              v-if="trending.increase"
                              fill-rule="evenodd"
                              d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                              clip-rule="evenodd"
                            />
                            <path
                              v-else-if="!trending.increase"
                              fill-rule="evenodd"
                              d="M5 10a1 1 0 011-1h8a1 1 0 110 2H6a1 1 0 01-1-1z"
                              clip-rule="evenodd"
                            />
                          </svg>
                          <span>${{ trending.price }}</span>
                        </div>
                      </td>
                      <td class="whitespace-nowrap">
                        <div>
                          <LineChart class="w-28 h-12 -mx-2" :datasets="trending.data" :increase="trending.increase" />
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        </div>
        <div class="w-1/3 overflow-hidden space-y-6 border-r border-gray-200 px-8">
          <div class="w-full flex items-center justify-between">
            <h3 class="font-medium">🚀 Top Gainers</h3>
            <a href="#" class="text-sm font-medium text-blue-500 flex items-center space-x-1">
              <span>More</span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-3 w-3"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
              </svg>
            </a>
          </div>
          <div class="flex flex-col">
            <div class="-my-2 overflow-x-auto sm:-mx-6 lg:-mx-8">
              <div class="py-2 align-middle inline-block min-w-full overflow-hidden">
                <table class="min-w-full">
                  <thead>
                    <tr>
                      <th class="text-left text-sm font-medium text-gray-500">Name</th>
                      <th class="text-left text-sm font-medium text-gray-500">Price</th>
                      <th class="text-left text-sm font-medium text-gray-500">Chart</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr v-for="topGainer in topGainers" :key="topGainer.id" class="border-b border-gray-200">
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center space-x-2">
                          <img :src="require(`~/assets/img/crypto-icon/${topGainer.logo}`)" alt="" />
                          <span>{{ topGainer.name }}</span>
                        </div>
                      </td>
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-4 w-4"
                            :class="[topGainer.increase ? 'text-emerald-500' : 'text-red-500']"
                            viewBox="0 0 20 20"
                            fill="currentColor"
                          >
                            <path
                              v-if="topGainer.increase"
                              fill-rule="evenodd"
                              d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                              clip-rule="evenodd"
                            />
                            <path
                              v-else-if="!topGainer.increase"
                              fill-rule="evenodd"
                              d="M5 10a1 1 0 011-1h8a1 1 0 110 2H6a1 1 0 01-1-1z"
                              clip-rule="evenodd"
                            />
                          </svg>
                          <span>${{ topGainer.price }}</span>
                        </div>
                      </td>
                      <td class="whitespace-nowrap">
                        <div>
                          <LineChart
                            class="w-28 h-12 -mx-2"
                            :datasets="topGainer.data"
                            :increase="topGainer.increase"
                          />
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        </div>
        <div class="w-1/3 overflow-hidden space-y-6 px-8">
          <div class="w-full flex items-center justify-between">
            <h3 class="font-medium">💎 Recently Added</h3>
            <a href="#" class="text-sm font-medium text-blue-500 flex items-center space-x-1">
              <span>More</span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-3 w-3"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
              </svg>
            </a>
          </div>
          <div class="flex flex-col">
            <div class="-my-2 overflow-x-auto sm:-mx-6 lg:-mx-8">
              <div class="py-2 align-middle inline-block min-w-full overflow-hidden">
                <table class="min-w-full">
                  <thead>
                    <tr>
                      <th class="text-left text-sm font-medium text-gray-500">Name</th>
                      <th class="text-left text-sm font-medium text-gray-500">Price</th>
                      <th class="text-left text-sm font-medium text-gray-500">Chart</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr v-for="recent in recents" :key="recent.id" class="border-b border-gray-200">
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center space-x-2">
                          <img :src="require(`~/assets/img/crypto-icon/${recent.logo}`)" alt="" />
                          <span>{{ recent.name }}</span>
                        </div>
                      </td>
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-4 w-4"
                            :class="[recent.increase ? 'text-emerald-500' : 'text-red-500']"
                            viewBox="0 0 20 20"
                            fill="currentColor"
                          >
                            <path
                              v-if="recent.increase"
                              fill-rule="evenodd"
                              d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                              clip-rule="evenodd"
                            />
                            <path
                              v-else-if="!recent.increase"
                              fill-rule="evenodd"
                              d="M5 10a1 1 0 011-1h8a1 1 0 110 2H6a1 1 0 01-1-1z"
                              clip-rule="evenodd"
                            />
                          </svg>
                          <span>${{ recent.price }}</span>
                        </div>
                      </td>
                      <td class="whitespace-nowrap">
                        <div>
                          <LineChart class="w-28 h-12 -mx-2" :datasets="recent.data" :increase="recent.increase" />
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Buy and trade section -->
    <section class="w-full my-24">
      <div class="relative max-w-screen-xl px-8 mx-auto grid grid-cols-12 gap-x-6">
        <div class="col-span-12 lg:col-span-6 mt-4 xl:mt-20 space-y-6 px-4">
          <h2 class="text-4xl font-semibold sm:pr-8 xl:pr-12">
            Buy & trade on the<br />
            original crypto exchange.
          </h2>
          <p class="text-gray-700 tracking-wide leading-relaxed">
            Buy now and get 40% extra bonus Minimum pre-sale amount 25 Crypto Coin. We accept BTC crypto-currency
          </p>
          <div class="space-y-6 pr-12">
            <div class="flex items-center space-x-4">
              <div class="w-full flex items-center relative px-5 py-3 border border-[#0c66ee] rounded-xl">
                <span class="text-sm font-medium pr-5 py-3 text-[#0c66ee] border-r border-[#0c66ee]"> Amount </span>
                <input
                  type="text"
                  class="w-full text-lg font-medium text-right border-none ring-0 focus:outline-none focus:ring-0"
                  name="url"
                  placeholder="5,000"
                />
              </div>
              <div class="flex items-center relative px-7 py-4 border border-[#0c66ee] rounded-xl">
                <img :src="require('~/assets/img/country-icon/eng.png')" class="w-8" />
                <select
                  name="country"
                  class="pr-7 text-sm font-medium border-none ring-0 focus:outline-none focus:ring-0"
                >
                  <option value="USD">USD</option>
                </select>
              </div>
            </div>
            <div class="flex items-center space-x-4">
              <div class="w-full flex items-center relative px-5 py-3 border border-[#0c66ee] rounded-xl">
                <span class="text-sm font-medium pr-5 py-3 text-[#0c66ee] border-r border-[#0c66ee]"> Get </span>
                <input
                  type="text"
                  class="w-full text-lg font-medium text-right border-none ring-0 focus:outline-none focus:ring-0"
                  name="url"
                  placeholder="0.10901"
                />
              </div>
              <div class="flex items-center relative px-6 py-4 border border-[#0c66ee] rounded-xl">
                <img :src="require('~/assets/img/crypto-icon/bitcoin.png')" class="w-8" />
                <select
                  name="country"
                  class="pr-7 text-sm font-medium border-none ring-0 focus:outline-none focus:ring-0"
                >
                  <option value="BTC">BTC</option>
                </select>
              </div>
            </div>
            <button class="w-full px-5 py-4 bg-blue-gradient rounded-full text-center text-white font-medium">
              Buy Now
            </button>
          </div>
        </div>
        <div class="col-span-12 lg:col-span-6">
          <div class="w-full">
            <img :src="require('~/assets/img/buy-and-trade.png')" class="-mt-4" alt="" />
          </div>
        </div>
      </div>
    </section>

    <!-- Partners section -->
    <section class="bg-partner relative max-w-full mx-10 my-24 shadow rounded-2xl overflow-hidden">
      <div class="w-full py-16 flex flex-col items-center justify-center space-y-4">
        <h3 class="text-2xl text-neutral-800 font-semibold">Trusted Partners Worldwide</h3>
        <p class="text-gray-700 tracking-wide leading-relaxed">
          We're partners with countless major organisations around the globe
        </p>
        <div class="flex items-center justify-center">
          <div>
            <img :src="require('~/assets/img/partner/clever.png')" class="w-72" alt="" />
          </div>
          <div>
            <img :src="require('~/assets/img/partner/clever.png')" class="w-72" alt="" />
          </div>
          <div>
            <img :src="require('~/assets/img/partner/clever.png')" class="w-72" alt="" />
          </div>
          <div>
            <img :src="require('~/assets/img/partner/clever.png')" class="w-72" alt="" />
          </div>
        </div>
      </div>
    </section>

    <!-- Credit card section -->
    <section class="w-full my-36">
      <div class="relative max-w-screen-xl px-8 mx-auto grid grid-cols-12 gap-x-6">
        <div class="col-span-12 lg:col-span-7">
          <div class="w-full">
            <img :src="require('~/assets/img/nefa-cc.png')" class="w-[95%]" alt="" />
          </div>
        </div>
        <div class="col-span-12 lg:col-span-5 space-y-6 px-6 mt-20">
          <h2 class="text-4xl font-semibold">Introducing the <span class="text-gradient">NEFA</span> Credit Card</h2>
          <p class="text-gray-700 tracking-wide leading-relaxed">
            Subject to cardholder and rewards terms which will be available at application.
          </p>
          <ul class="space-y-2">
            <li class="flex items-center space-x-2">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-5 w-5 text-[#0c66ee]"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  fill-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  clip-rule="evenodd"
                />
              </svg>
              <span>Up to 3% back on purchases</span>
            </li>
            <li class="flex items-center space-x-2">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-5 w-5 text-[#0c66ee]"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  fill-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  clip-rule="evenodd"
                />
              </svg>
              <span>Earn rewards in bitcoin or any crypto on NEFA</span>
            </li>
            <li class="flex items-center space-x-2">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-5 w-5 text-[#0c66ee]"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  fill-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  clip-rule="evenodd"
                />
              </svg>
              <span>No annual fee</span>
            </li>
          </ul>
          <button class="px-10 py-4 text-center bg-inherit text-gradient rounded-full border border-[#0c66ee]">
            Join the waitlist
          </button>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      trendings: [
        {
          id: 1,
          name: 'Bitcoin',
          price: 43180.13,
          logo: 'bitcoin.png',
          increase: true,
          data: [40, 35, 60, 75, 60, 75, 50],
        },
        {
          id: 2,
          name: 'Ethereum',
          price: 3480.65,
          logo: 'ethereum.png',
          increase: false,
          data: [25, 30, 60, 50, 80, 55, 80],
        },
        {
          id: 3,
          name: 'Solana',
          price: 150.2,
          logo: 'solana.png',
          increase: true,
          data: [40, 45, 40, 80, 50, 60, 35],
        },
        {
          id: 4,
          name: 'Dogecoin',
          price: 0.1572,
          logo: 'dogecoin.png',
          increase: true,
          data: [35, 70, 60, 80, 50, 60, 40],
        },
      ],
      topGainers: [
        {
          id: 1,
          name: 'PAPPAY',
          price: 0.00374,
          logo: 'pappay.png',
          increase: true,
          data: [30, 50, 45, 60, 70, 40, 45],
        },
        {
          id: 2,
          name: 'Bitcoin Asia',
          price: 0.02096,
          logo: 'bitcoin-asia.png',
          increase: true,
          data: [25, 60, 50, 60, 35, 50, 70],
        },
        {
          id: 3,
          name: 'MoonRock',
          price: 0.004907,
          logo: 'moonrock.png',
          increase: true,
          data: [40, 35, 40, 25, 50, 70, 45],
        },
        {
          id: 4,
          name: 'NinjaFloki',
          price: 0.000123,
          logo: 'ninjafloki.png',
          increase: true,
          data: [45, 35, 40, 30, 25, 45, 35],
        },
      ],
      recents: [
        {
          id: 1,
          name: 'MetaCraft',
          price: 0.0608,
          logo: 'metacraft.png',
          increase: false,
          data: [40, 50, 45, 60, 35, 40, 45],
        },
        {
          id: 2,
          name: 'Frog',
          price: 0.5875,
          logo: 'frog.png',
          increase: false,
          data: [25, 50, 45, 48, 40, 60, 45],
        },
        {
          id: 3,
          name: 'Musk Doge',
          price: 0.04041,
          logo: 'musk-doge.png',
          increase: true,
          data: [25, 35, 60, 45, 50, 45, 45],
        },
        {
          id: 4,
          name: '2SHARE',
          price: 1366.24,
          logo: '2share.png',
          increase: true,
          data: [35, 30, 60, 50, 35, 45, 40],
        },
      ],
    }
  },
}
</script>
<style scoped>
.text-header-gradient {
  background: rgb(57, 132, 244);
  background: linear-gradient(169.4deg, #3984f4 -6.01%, #0cd3ff 36.87%, #2f7cf0 78.04%, #0e65e8 103.77%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.bg-partner {
  background: url('../assets/img/partner/background.png');
  background-size: cover;
  background-position: center;
}
</style>
