<template>
  <div class="max-w-[280px] xl:max-w-[363px] space-y-6 sm:space-y-3 text-center">
    <img :src="require(`~/assets/img/getting-started/${step.img}`)" class="max-w-[245px] mx-auto" alt="" />
    <h3 class="text-xl text-neutral-800 font-semibold">{{ step.title }}</h3>
    <p class="text-sm text-gray-700 leading-relaxed">
      {{ step.description }}
    </p>
  </div>
</template>
<script>
export default {
  name: 'LandingStep',
  props: {
    step: {
      type: Object,
      required: true,
    },
  },
}
</script>
