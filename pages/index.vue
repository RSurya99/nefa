<template>
  <div class="w-full">
    <!-- Hero section -->
    <section id="hero" class="w-full pb-24">
      <BaseSection>
        <div class="col-span-12 lg:col-span-6 mt-12 xl:mt-10 space-y-4 sm:space-y-6 px-6 text-center sm:text-left">
          <span data-aos="fade-right" data-aos-once="true" class="text-base text-gradient font-semibold uppercase"
            >The Spotify of Museums</span
          >
          <h1
            data-aos="fade-right"
            data-aos-once="true"
            class="text-[2.5rem] sm:text-5xl xl:text-6xl font-bold leading-tight capitalize sm:pr-8 xl:pr-10"
          >
            The World's <span class="text-header-gradient">First</span> AI tour guide
          </h1>
          <p data-aos="fade-down" data-aos-once="true" data-aos-delay="300" class="paragraph hidden sm:block">
            Explore museums like never before! Interactive, engaging tours. Your personal guide to art, history, and culture. Join us and explore now!          </p>
          <div
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-delay="700"
            class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4 mt-2"
          >
            <BaseButton
              class="max-w-full px-8 py-4 bg-gradient-to-r from-[#468ef9] to-[#0c66ee] border border-[#0c66ee] text-white"
            >
            <form action="https://docs.google.com/forms/d/e/1FAIpQLSfxLB0IGPnvEW6sIoKJiYomXEfPkOtoAzRJo8WIJpKqmYOgOA/viewform?usp=sf_link" target="_blank">
              <input type="submit" value="Contact Us" />
            </form>

            </BaseButton>
            <!-- <BaseButton
              class="max-w-full px-6 py-4 bg-inherit text-gradient border border-[#0c66ee] flex items-center justify-center"
            >
              <span>Download App</span>
              <ChevronDownIcon :size="20" class="mt-1 text-[#0c66ee]" />
            </BaseButton> -->
          </div>
        </div>
        <div class="hidden sm:block col-span-12 lg:col-span-6">
          <div class="w-full">
            <img
              data-aos="fade-up"
              data-aos-once="true"
              :src="require('~/assets/img/museye-herogrid.png')"
              class="margin-top: 0.5rem"
              alt=""
            />
          </div>
        </div>
        <!-- <img
          data-aos="fade-up"
          data-aos-delay="300"
          :src="require('~/assets/img/pattern/ellipse-1.png')"
          class="hidden sm:block absolute bottom-12 xl:bottom-16 left-4 xl:left-0 w-6"
        /> -->
        <img
          data-aos="fade-up"
          data-aos-delay="300"
          :src="require('~/assets/img/pattern/ellipse-2.png')"
          class="hidden sm:block absolute top-4 sm:top-10 right-64 sm:right-96 xl:right-[32rem] w-6"
        />
        <img
          data-aos="fade-up"
          data-aos-delay="300"
          :src="require('~/assets/img/pattern/ellipse-3.png')"
          class="hidden sm:block absolute bottom-56 right-24 w-6"
        />
        <!-- <img
          data-aos="fade-up"
          data-aos-delay="300"
          :src="require('~/assets/img/pattern/star.png')"
          class="hidden sm:block absolute top-20 sm:top-28 right-16 lg:right-0 lg:left-[30rem] w-8"
        /> -->
      </BaseSection>
    </section>

    <!-- Crypto statistic section -->
    <!-- <section
      class="max-w-screen-xl mx-2 sm:mx-auto px-4 sm:px-6 lg:px-0 py-6 pb-20 sm:py-8 rounded-[2.25rem] sm:rounded-xl bg-white shadow-lg sm:shadow-md transform lg:-translate-y-12"
    >
      <div class="w-full flex flex-col lg:flex-row items-center justify-center">
        <LandingCryptoStatistic
          data-aos="fade-up"
          title="🔥 Trending"
          :datasets="trendings"
          class="xl:border-r border-gray-200 lg:px-8"
        />
        <LandingCryptoStatistic
          data-aos="fade-up"
          data-aos-delay="150"
          title="🚀 Top Gainers"
          :datasets="topGainers"
          class="xl:border-r border-gray-200 lg:px-8"
        />
        <LandingCryptoStatistic
          data-aos="fade-up"
          data-aos-delay="300"
          title="💎 Recently Added"
          :datasets="recents"
          class="lg:px-8"
        />
      </div>
    </section> -->

    <!-- Buy and trade section -->
    <!-- <section class="w-full my-24">
      <BaseSection>
        <LandingBuyTradeImage class="sm:hidden mb-8" />
        <div data-aos="fade-right" class="col-span-12 lg:col-span-6 mt-4 xl:mt-20 space-y-6 px-4">
          <h2 class="text-4xl font-semibold sm:pr-8 xl:pr-12">
            Buy & trade on the <br class="hidden sm:block" />
            original crypto exchange.
          </h2>
          <p class="paragraph">
            Buy now and get 40% extra bonus Minimum pre-sale amount 25 Crypto Coin. We accept BTC crypto-currency
          </p>
          <div class="space-y-6 lg:pr-12">
            <LandingExchange
              title="Amount"
              name="amount"
              type="number"
              default-value="5.000"
              :exchange-selected="currencySelected"
              :exchanges="currencies"
            />
            <LandingExchange
              title="Get"
              name="get"
              type="number"
              default-value="0.10901"
              :exchange-selected="cryptoSelected"
              :exchanges="cryptocurrencies"
            />
            <BaseButton class="w-full px-5 py-4 bg-blue-gradient text-white text-base font-medium">Buy Now</BaseButton>
          </div>
        </div>
        <LandingBuyTradeImage data-aos="fade-left" class="hidden sm:block" />
      </BaseSection>
    </section> -->

    <!-- Partners section -->
    <section class="bg-partner relative max-w-full sm:mx-6 my-24 shadow sm:rounded-2xl overflow-hidden">
      <div class="w-full px-6 sm:px-0 py-16 flex flex-col items-center justify-center space-y-4 text-center">
        <h3 data-aos="flip-down" class="text-2xl text-neutral-800 font-semibold">Trusted Partners </h3>
        <p data-aos="flip-down" class="paragraph">We're partners with countless major organisations</p>
        <div data-aos="fade-up" class="flex flex-wrap items-center justify-center">
          <LandingPartnerImage
            v-for="img in ['BPL.png', 'btulogo.png', 'microsoft.png']"
            :key="img"
            :img="img"
          />
        </div>
      </div>
    </section>

    <!-- Credit card section -->
    <section class="w-full my-36">
      <BaseSection data-aos="fade-down">
        <div class="col-span-14 lg:col-span-7">
          <div class="w-full">
            <img :src="require('~/assets/img/Museyeintro.png')" class=" w-[95%]" alt="" />
          </div>
        </div>
        <div class="col-span-12 lg:col-span-5 space-y-6 px-4 sm:px-6 mt-20">
          <h2 id="aiintro" class="text-4xl font-semibold">
            Introducing  <span class="text-header-gradient">Museye</span> AI tour guide
          </h2>
          <p class="paragraph">The spotify of museums</p>
          <ul class="space-y-4 sm:space-y-2">
            <LandingListItem title="Explore, plan and book your visits" />
            <LandingListItem title="Keep track of your museums visits and save your memories!" />
            <LandingListItem title="Personalised experience to each and every users!" />
          </ul>
          <BaseButton
            class="w-full sm:max-w-[240px] px-10 py-4 bg-inherit text-gradient border border-[#0c66ee] text-base"
            >
            <form action="https://docs.google.com/forms/d/e/1FAIpQLSfHjCpWTOVkssY6buB7FbkBZ97BE1ngYVuXUcjW9bqDI4wKGg/viewform?usp=sf_link" target="_blank">
              <input type="submit" value="Join our waiting list" />
            </form></BaseButton
          >
        </div>
      </BaseSection>
    </section>

    <!-- Advanced trading tools section -->
    <section class="bg-trading-tools relative max-w-full sm:mx-4 my-20 py-16 shadow rounded-2xl overflow-hidden">
      <div class="relative max-w-screen-xl px-4 sm:px-2 mx-auto grid grid-cols-12 gap-x-6">
        <LandingTradingToolImage class="sm:hidden" />
        <div data-aos="fade-right" class="col-span-12 lg:col-span-6 space-y-8 sm:space-y-6 px-4 sm:px-6 mt-8">
          <h2 class="text-4xl font-semibold">Museums Education <span class="text-header-gradient">4.0</span></h2>
          <div class="space-y-2">
            <h4 class="text-lg font-medium">The spotify of museums</h4>
            <p class="paragraph text-sm xl:text-base">
              Elevate your cultural journey! Stay updated with exhibitions you love. Our platform connects you to museums and galleries, keeping you in sync with the art and culture scene. Experience the pulse of creativity and heritage seamlessly.            </p>
          </div>
          <div class="space-y-2">
            <h4 class="text-lg font-medium">Personalised experience for each and every visitor</h4>
            <p class="paragraph text-sm xl:text-base">
              Revolutionize your museum visit! Personalized experiences for all <strong>ages</strong>, <strong>languages</strong>, and <strong>level of interest</strong> using advanced AI. Make every tour unique and engaging.

            </p>
          </div>
          <div class="space-y-2">
            <h4 class="text-lg font-medium">Acceessable museums for everyone!</h4>
            <p class="paragraph text-sm xl:text-base">
              Enhanced accessibility in museums worldwide. Tailored services for <strong>visitors with visual and auditory impairments</strong>. Experience art and history inclusively and effortlessly. Dedicated support ensuring a seamless and enriching visit.            </p>
          </div>
          <div class="flex flex-col sm:flex-row">
            <!-- <BaseButton class="px-10 py-4 bg-inherit text-gradient border border-[#4A8FF6] text-base">
              Get Started
            </BaseButton>
            <BaseButton class="bg-inherit text-[#4A8FF6] px-10 py-4 text-center underline rounded-full">
              Learn More
            </BaseButton> -->
          </div>
        </div>
        <LandingTradingToolImage data-aos="fade-left" class="hidden sm:block" />
      </div>
    </section>

    <!-- Industry-leading security section -->
    <!-- <section class="w-full my-24">
      <div class="relative max-w-screen-xl px-8 mx-auto grid grid-cols-12 gap-x-6">
        <div data-aos="fade-right" class="col-span-12 lg:col-span-6">
          <div class="w-full">
            <img :src="require('~/assets/img/industry-leading-security.webp')" class="w-full" alt="" />
          </div>
        </div>
        <div data-aos="fade-left" class="col-span-12 lg:col-span-5 space-y-8 sm:space-y-6 mt-8 xl:px-8">
          <h2 class="text-4xl font-semibold">Industry-leading security from day one</h2>
          <ul class="space-y-8 sm:space-y-4">
            <LandingListItem title="Safety, security and compliance">
              <p class="text-sm text-gray-700 leading-relaxed">
                NEFA is a licensed New York trust company that undergoes regular bank exams and is subject to the
                cybersecurity audits conducted by the New York Department of Financial Services.
                <span class="underline">Learn more</span> about our commitment to security.
              </p>
            </LandingListItem>
            <LandingListItem title="Hardware security keys">
              <p class="text-sm text-gray-700 leading-relaxed">
                With NEFA you can secure your account with a hardware security key via WebAuthn.
              </p>
            </LandingListItem>
            <LandingListItem title="SOC Certifications">
              <p class="text-sm text-gray-700 leading-relaxed">
                NEFA is <span class="underline">SOC 1 Type 2</span> and
                <span class="underline">SOC 2 Type 2</span> compliant. We are the world’s first cryptocurrency exchange
                and custodian to complete these exams.
              </p>
            </LandingListItem>
          </ul>
        </div>
      </div>
    </section> -->

    <!-- Getting started section -->
    <section class="bg-trading-tools relative max-w-full sm:mx-4 xl:mx-10 my-24 shadow sm:rounded-2xl overflow-hidden">
      <div class="w-full py-16 flex flex-col items-center">
        <h2 data-aos="flip-down" class="text-3xl sm:text-4xl font-semibold text-center">
            Get to know our super team!        </h2>
        <div
          data-aos="fade-up"
          class="relative w-full flex flex-col lg:flex-row items-center justify-between space-y-12 lg:space-y-0 px-4 xl:px-10 mt-16 sm:mt-8"
        >
          <LandingStep v-for="step in steps" :key="step.title" :step="step" />
          <!-- <img
            :src="require('~/assets/img/getting-started/arrow.png')"
            class="hidden lg:inline-block absolute top-32 left-64 xl:left-[22rem] w-24 xl:w-[9.5rem]"
            alt=""
          /> -->
          <!-- <img
            :src="require('~/assets/img/getting-started/arrow.png')"
            class="hidden lg:inline-block absolute top-32 right-64 xl:right-[22rem] w-24 xl:w-[9.5rem]"
            alt=""
          /> -->
        </div>
      </div>
    </section>

    <!-- FAQ section -->
    <!-- <section class="w-full my-24">
      <BaseSection>
        <div data-aos="fade-right" data-aos-delay="150" class="col-span-12 lg:col-span-6">
          <div class="w-full">
            <img :src="require('~/assets/img/faq.webp')" class="w-full" alt="" />
          </div>
        </div>
        <div data-aos="fade-left" data-aos-delay="150" class="col-span-12 lg:col-span-6 px-4 sm:px-6 mt-8">
          <span class="text-base text-gradient font-semibold uppercase mb-4 sm:mb-2">Support</span>
          <h2 class="text-3xl sm:text-4xl font-semibold mb-10 sm:mb-6">Frequently asked questions</h2>

          <ul class="shadow-box">
            <BaseAccordion v-for="(accordion, index) in accordions" :key="index" :accordion="accordion" />
          </ul>
        </div>
      </BaseSection>
    </section> -->

    <!-- <div class="w-full my-10 flex justify-center">
      <a
        v-smooth-scroll
        data-aos="flip-down"
        data-aos-delay="150"
        href="#navbar"
        class="px-6 py-3 flex items-center space-x-2 bg-[#FAFAFA] hover:bg-gray-100 hover:shadow-md border border-[#DDDDDD] rounded-md text-gray-700"
      >
        <span>Back to top</span>
        <ArrowUpIcon :size="20" />
      </a>
    </div> -->
  </div>
</template>

<script>
import aosMixin from '@/mixins/aos'
export default {
  name: 'IndexPage',
  mixins: [aosMixin],
  data() {
    return {
      selected: 0,
      dropdownConcurency: false,
      dropdownCrypto: false,
      currencySelected: {
        img: 'country-icon/eng.png',
        name: 'USD',
      },
      // currencies: [
      //   {
      //     img: 'country-icon/eng.png',
      //     name: 'USD',
      //   },
      // ],
      // cryptoSelected: {
      //   img: 'crypto-icon/bitcoin.png',
      //   name: 'BTC',
      // },
      // cryptocurrencies: [
      //   {
      //     img: 'crypto-icon/bitcoin.png',
      //     name: 'BTC',
      //   },
      // ],
      // trendings: [
      //   {
      //     id: 1,
      //     name: 'Bitcoin',
      //     price: 43180.13,
      //     logo: 'bitcoin.png',
      //     increase: true,
      //     data: [40, 35, 60, 75, 60, 75, 50],
      //   },
      //   {
      //     id: 2,
      //     name: 'Ethereum',
      //     price: 3480.65,
      //     logo: 'ethereum.png',
      //     increase: false,
      //     data: [25, 30, 60, 50, 80, 55, 80],
      //   },
      //   {
      //     id: 3,
      //     name: 'Solana',
      //     price: 150.2,
      //     logo: 'solana.png',
      //     increase: true,
      //     data: [40, 45, 40, 80, 50, 60, 35],
      //   },
      //   {
      //     id: 4,
      //     name: 'Dogecoin',
      //     price: 0.1572,
      //     logo: 'dogecoin.png',
      //     increase: true,
      //     data: [35, 70, 60, 80, 50, 60, 40],
      //   },
      // ],
      // topGainers: [
      //   {
      //     id: 1,
      //     name: 'PAPPAY',
      //     price: 0.00374,
      //     logo: 'pappay.png',
      //     increase: true,
      //     data: [30, 50, 45, 60, 70, 40, 45],
      //   },
      //   {
      //     id: 2,
      //     name: 'Bitcoin Asia',
      //     price: 0.02096,
      //     logo: 'bitcoin-asia.png',
      //     increase: true,
      //     data: [25, 60, 50, 60, 35, 50, 70],
      //   },
      //   {
      //     id: 3,
      //     name: 'MoonRock',
      //     price: 0.004907,
      //     logo: 'moonrock.png',
      //     increase: true,
      //     data: [40, 35, 40, 25, 50, 70, 45],
      //   },
      //   {
      //     id: 4,
      //     name: 'NinjaFloki',
      //     price: 0.000123,
      //     logo: 'ninjafloki.png',
      //     increase: true,
      //     data: [45, 35, 40, 30, 25, 45, 35],
      //   },
      // ],
      // recents: [
      //   {
      //     id: 1,
      //     name: 'MetaCraft',
      //     price: 0.0608,
      //     logo: 'metacraft.png',
      //     increase: false,
      //     data: [40, 50, 45, 60, 35, 40, 45],
      //   },
      //   {
      //     id: 2,
      //     name: 'Frog',
      //     price: 0.5875,
      //     logo: 'frog.png',
      //     increase: false,
      //     data: [25, 50, 45, 48, 40, 60, 45],
      //   },
      //   {
      //     id: 3,
      //     name: 'Musk Doge',
      //     price: 0.04041,
      //     logo: 'musk-doge.png',
      //     increase: true,
      //     data: [25, 35, 60, 45, 50, 45, 45],
      //   },
      //   {
      //     id: 4,
      //     name: '2SHARE',
      //     price: 1366.24,
      //     logo: '2share.png',
      //     increase: true,
      //     data: [35, 30, 60, 50, 35, 45, 40],
      //   },
      // ],
      accordions: [
        {
          title: 'Why should I choose NEFA?',
          description:
            "We're industry pioneers, having been in the cryptocurrency industry since 2016. We've facilitated more than 21 billion USD worth of transactions on our exchange for customers in over 40 countries. Today, we're trusted by over 8 million customers around the world and have received praise for our easy-to-use app, secure wallet, and range of features.",
        },
        {
          title: 'How secure is NEFA?',
          description:
            "We're industry pioneers, having been in the cryptocurrency industry since 2016. We've facilitated more than 21 billion USD worth of transactions on our exchange for customers in over 40 countries. Today, we're trusted by over million customers around the world and have received praise for our easy-to-use app, secure wallet, and range of features.",
        },
        {
          title: 'Do I have to buy a whole Bitcoin?',
          description:
            "We're industry pioneers, having been in the cryptocurrency industry since 2016. We've facilitated more than 21 billion USD worth of transactions on our exchange for customers in over 40 countries. Today, we're trusted by over million customers around the world and have received praise for our easy-to-use app, secure wallet, and range of features.",
        },
        {
          title: 'How do I actually buy Bitcoin?',
          description:
            "We're industry pioneers, having been in the cryptocurrency industry since 2016. We've facilitated more than 21 billion USD worth of transactions on our exchange for customers in over 40 countries. Today, we're trusted by over million customers around the world and have received praise for our easy-to-use app, secure wallet, and range of features.",
        },
      ],
      steps: [
        {
          img: 'Artur.png',
          title: 'Artur Schröder',
          description:
            'E-Business specialist, Product Manager, and software manager',
        },
        {
          img: 'Zeyn.png',
          title: 'Zeyn Hassan',
          description:
            'Former Historian, Museum Expert and a current Software Develoepr',
        },
        // {
        //   img: 'buy-crypto.png',
        //   title: 'Buy Crypto',
        //   description:
        //     'Buy Bitcoin or Ethereum, then securely store it in your Wallet or send it on easily to your friends anywhere',
        // },
      ],
    }
  },
}
</script>
<style scoped>
.text-header-gradient {
  background: rgb(110, 41, 151);
  background: linear-gradient(169.4deg, #3984f4 -6.01%, #0cd3ff 36.87%, #2f7cf0 78.04%, #0e65e8 103.77%);
  background-clip: text;
  -webkit-text-fill-color: transparent;
}
.bg-partner {
  background: url('../assets/img/partner/background.png');
  background-size: cover;
  background-position: center;
}
.bg-trading-tools {
  background: url('../assets/img/bg-trading-tools.webp');
  background-size: cover;
  background-position: center;
}
.max-h-0 {
  max-height: 0;
}
</style>
