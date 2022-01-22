<template>
  <div class="min-h-screen font-sans antialiased relative">
    <div class="relative">
      <div class="absolute top-0 left-0 w-full h-[225vh] lg:h-[125vh] cover-gradient"></div>
      <BaseNavbar />

      <main class="text-neutral-800">
        <Nuxt />
      </main>

      <BaseFooter />
    </div>
  </div>
</template>
<script>
export default {
  name: 'DefaultLayout',
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
