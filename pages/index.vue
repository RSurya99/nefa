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

    <section
      class="max-w-screen-xl mx-auto px-10 lg:px-0 py-6 sm:py-8 rounded-lg bg-white shadow-md transform lg:-translate-y-10"
    >
      <div class="w-full flex flex-col lg:flex-row items-center justify-center space-y-6 lg:space-y-0 lg:space-x-8">
        <div class="w-1/3 space-y-6 border-r border-gray-200 px-6">
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
              <div class="py-2 align-middle inline-block min-w-full sm:px-6 lg:px-8 overflow-hidden">
                <table class="min-w-full">
                  <thead>
                    <tr>
                      <th class="text-left text-sm font-medium text-gray-500">Name</th>
                      <th class="text-left text-sm font-medium text-gray-500">Price</th>
                      <th class="text-left text-sm font-medium text-gray-500">Chart</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr class="border-b border-gray-200">
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center space-x-2">
                          <img :src="require('~/assets/img/crypto-icon/bitcoin.png')" alt="" />
                          <span>Bitcoin</span>
                        </div>
                      </td>
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-4 w-4 text-emerald-500"
                            viewBox="0 0 20 20"
                            fill="currentColor"
                          >
                            <path
                              fill-rule="evenodd"
                              d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                              clip-rule="evenodd"
                            />
                          </svg>
                          <span>$43,180.13</span>
                        </div>
                      </td>
                      <td class="whitespace-nowrap">
                        <div>
                          <LineChart class="w-28 h-12 -mx-2 -mt-4" />
                        </div>
                      </td>
                    </tr>
                    <tr class="border-b border-gray-200">
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center space-x-2">
                          <img :src="require('~/assets/img/crypto-icon/bitcoin.png')" alt="" />
                          <span>Bitcoin</span>
                        </div>
                      </td>
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-4 w-4 text-emerald-500"
                            viewBox="0 0 20 20"
                            fill="currentColor"
                          >
                            <path
                              fill-rule="evenodd"
                              d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                              clip-rule="evenodd"
                            />
                          </svg>
                          <span>$43,180.13</span>
                        </div>
                      </td>
                      <td class="whitespace-nowrap">
                        <div>
                          <LineChart class="w-28 h-12 -mx-2 -mt-4" />
                        </div>
                      </td>
                    </tr>
                    <tr class="border-b border-gray-200">
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center space-x-2">
                          <img :src="require('~/assets/img/crypto-icon/bitcoin.png')" alt="" />
                          <span>Bitcoin</span>
                        </div>
                      </td>
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-4 w-4 text-emerald-500"
                            viewBox="0 0 20 20"
                            fill="currentColor"
                          >
                            <path
                              fill-rule="evenodd"
                              d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                              clip-rule="evenodd"
                            />
                          </svg>
                          <span>$43,180.13</span>
                        </div>
                      </td>
                      <td class="whitespace-nowrap">
                        <div>
                          <LineChart class="w-28 h-12 -mx-2 -mt-4" />
                        </div>
                      </td>
                    </tr>
                    <tr class="border-b border-gray-200">
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center space-x-2">
                          <img :src="require('~/assets/img/crypto-icon/bitcoin.png')" alt="" />
                          <span>Bitcoin</span>
                        </div>
                      </td>
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-4 w-4 text-emerald-500"
                            viewBox="0 0 20 20"
                            fill="currentColor"
                          >
                            <path
                              fill-rule="evenodd"
                              d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                              clip-rule="evenodd"
                            />
                          </svg>
                          <span>$43,180.13</span>
                        </div>
                      </td>
                      <td class="whitespace-nowrap">
                        <div>
                          <LineChart class="w-28 h-12 -mx-2 -mt-4" />
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        </div>
        <div class="w-1/3 space-y-6 border-r border-gray-200 px-6">
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
              <div class="py-2 align-middle inline-block min-w-full sm:px-6 lg:px-8 overflow-hidden">
                <table class="min-w-full">
                  <thead>
                    <tr>
                      <th class="text-left text-sm font-medium text-gray-500">Name</th>
                      <th class="text-left text-sm font-medium text-gray-500">Price</th>
                      <th class="text-left text-sm font-medium text-gray-500">Chart</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr class="border-b border-gray-200">
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center space-x-2">
                          <img :src="require('~/assets/img/crypto-icon/bitcoin.png')" alt="" />
                          <span>Bitcoin</span>
                        </div>
                      </td>
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-4 w-4 text-emerald-500"
                            viewBox="0 0 20 20"
                            fill="currentColor"
                          >
                            <path
                              fill-rule="evenodd"
                              d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                              clip-rule="evenodd"
                            />
                          </svg>
                          <span>$43,180.13</span>
                        </div>
                      </td>
                      <td class="whitespace-nowrap">
                        <div>
                          <LineChart class="w-28 h-12 -mx-2 -mt-4" />
                        </div>
                      </td>
                    </tr>
                    <tr class="border-b border-gray-200">
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center space-x-2">
                          <img :src="require('~/assets/img/crypto-icon/bitcoin.png')" alt="" />
                          <span>Bitcoin</span>
                        </div>
                      </td>
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-4 w-4 text-emerald-500"
                            viewBox="0 0 20 20"
                            fill="currentColor"
                          >
                            <path
                              fill-rule="evenodd"
                              d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                              clip-rule="evenodd"
                            />
                          </svg>
                          <span>$43,180.13</span>
                        </div>
                      </td>
                      <td class="whitespace-nowrap">
                        <div>
                          <LineChart class="w-28 h-12 -mx-2 -mt-4" />
                        </div>
                      </td>
                    </tr>
                    <tr class="border-b border-gray-200">
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center space-x-2">
                          <img :src="require('~/assets/img/crypto-icon/bitcoin.png')" alt="" />
                          <span>Bitcoin</span>
                        </div>
                      </td>
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-4 w-4 text-emerald-500"
                            viewBox="0 0 20 20"
                            fill="currentColor"
                          >
                            <path
                              fill-rule="evenodd"
                              d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                              clip-rule="evenodd"
                            />
                          </svg>
                          <span>$43,180.13</span>
                        </div>
                      </td>
                      <td class="whitespace-nowrap">
                        <div>
                          <LineChart class="w-28 h-12 -mx-2 -mt-4" />
                        </div>
                      </td>
                    </tr>
                    <tr class="border-b border-gray-200">
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center space-x-2">
                          <img :src="require('~/assets/img/crypto-icon/bitcoin.png')" alt="" />
                          <span>Bitcoin</span>
                        </div>
                      </td>
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-4 w-4 text-emerald-500"
                            viewBox="0 0 20 20"
                            fill="currentColor"
                          >
                            <path
                              fill-rule="evenodd"
                              d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                              clip-rule="evenodd"
                            />
                          </svg>
                          <span>$43,180.13</span>
                        </div>
                      </td>
                      <td class="whitespace-nowrap">
                        <div>
                          <LineChart class="w-28 h-12 -mx-2 -mt-4" />
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        </div>
        <div class="w-1/3 space-y-6 border-r border-gray-200 px-6">
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
              <div class="py-2 align-middle inline-block min-w-full sm:px-6 lg:px-8 overflow-hidden">
                <table class="min-w-full">
                  <thead>
                    <tr>
                      <th class="text-left text-sm font-medium text-gray-500">Name</th>
                      <th class="text-left text-sm font-medium text-gray-500">Price</th>
                      <th class="text-left text-sm font-medium text-gray-500">Chart</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr class="border-b border-gray-200">
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center space-x-2">
                          <img :src="require('~/assets/img/crypto-icon/bitcoin.png')" alt="" />
                          <span>Bitcoin</span>
                        </div>
                      </td>
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-4 w-4 text-emerald-500"
                            viewBox="0 0 20 20"
                            fill="currentColor"
                          >
                            <path
                              fill-rule="evenodd"
                              d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                              clip-rule="evenodd"
                            />
                          </svg>
                          <span>$43,180.13</span>
                        </div>
                      </td>
                      <td class="whitespace-nowrap">
                        <div>
                          <LineChart class="w-28 h-12 -mx-2 -mt-4" />
                        </div>
                      </td>
                    </tr>
                    <tr class="border-b border-gray-200">
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center space-x-2">
                          <img :src="require('~/assets/img/crypto-icon/bitcoin.png')" alt="" />
                          <span>Bitcoin</span>
                        </div>
                      </td>
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-4 w-4 text-emerald-500"
                            viewBox="0 0 20 20"
                            fill="currentColor"
                          >
                            <path
                              fill-rule="evenodd"
                              d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                              clip-rule="evenodd"
                            />
                          </svg>
                          <span>$43,180.13</span>
                        </div>
                      </td>
                      <td class="whitespace-nowrap">
                        <div>
                          <LineChart class="w-28 h-12 -mx-2 -mt-4" />
                        </div>
                      </td>
                    </tr>
                    <tr class="border-b border-gray-200">
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center space-x-2">
                          <img :src="require('~/assets/img/crypto-icon/bitcoin.png')" alt="" />
                          <span>Bitcoin</span>
                        </div>
                      </td>
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-4 w-4 text-emerald-500"
                            viewBox="0 0 20 20"
                            fill="currentColor"
                          >
                            <path
                              fill-rule="evenodd"
                              d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                              clip-rule="evenodd"
                            />
                          </svg>
                          <span>$43,180.13</span>
                        </div>
                      </td>
                      <td class="whitespace-nowrap">
                        <div>
                          <LineChart class="w-28 h-12 -mx-2 -mt-4" />
                        </div>
                      </td>
                    </tr>
                    <tr class="border-b border-gray-200">
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center space-x-2">
                          <img :src="require('~/assets/img/crypto-icon/bitcoin.png')" alt="" />
                          <span>Bitcoin</span>
                        </div>
                      </td>
                      <td class="py-4 whitespace-nowrap">
                        <div class="flex items-center">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-4 w-4 text-emerald-500"
                            viewBox="0 0 20 20"
                            fill="currentColor"
                          >
                            <path
                              fill-rule="evenodd"
                              d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                              clip-rule="evenodd"
                            />
                          </svg>
                          <span>$43,180.13</span>
                        </div>
                      </td>
                      <td class="whitespace-nowrap">
                        <div>
                          <LineChart class="w-28 h-12 -mx-2 -mt-4" />
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
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      chartData: {
        datasets: [
          {
            borderColor: '#4bcc96',
            borderWidth: 2,
            data: [30, 50, 100, 1000, 20, 50],
          },
        ],
      },
      chartOptions: {
        responsive: true,
        maintainAspectRatio: false,
        legend: {
          display: false,
        },
        tooltips: {
          callbacks: {
            label: (tooltipItem) => {
              return tooltipItem.yLabel
            },
          },
        },
        scales: {
          yAxes: [
            {
              ticks: {
                display: false,
              },
              gridLines: {
                drawBorder: false,
                // color: 'rgba(0, 0, 0, 0)',
              },
            },
          ],
        },
      },
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
</style>
