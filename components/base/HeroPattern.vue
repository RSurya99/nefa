<template>
  <div>
    <img
      :src="require('~/assets/img/pattern/ellipse-1.png')"
      class="hidden sm:block absolute bottom-12 xl:bottom-16 left-4 xl:left-0 w-6"
    />
    <img
      :src="require('~/assets/img/pattern/ellipse-2.png')"
      class="hidden sm:block absolute top-4 sm:top-10 right-64 sm:right-96 xl:right-[32rem] w-6"
    />
    <img :src="require('~/assets/img/pattern/ellipse-3.png')" class="hidden sm:block absolute bottom-56 right-24 w-6" />
    <img
      :src="require('~/assets/img/pattern/star.png')"
      class="hidden sm:block absolute top-20 sm:top-28 right-16 lg:right-0 lg:left-[30rem] w-8"
    />
  </div>
</template>
<script>
export default {
  name: 'BaseHeroPattern',
}
</script>
