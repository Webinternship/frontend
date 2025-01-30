<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="bg-gradient-to-r from-yellow-100 to-green-300">
    <svg viewBox="0 0 1440 200" class="fill-black">
      <path d="M0,132C180,0,1360,160,1440,0L140,0L0,0Z"></path>
    </svg>

    <section class="flex items-center justify-center">
      <h2 class="text-center">{{ networking }}</h2>
      <div class="w-72 flex gap-32">
        <lottie-player src="./cyber.json" speed="1" autoplay loop></lottie-player>
        <lottie-player src="./machine-learning.json" speed="1" autoplay loop></lottie-player>
      </div>
      <p class="text-center">{{ networking }}</p>
    </section>

    <svg viewBox="0 0 1440 200" class="fill-gray-300">
      <path
        d="M0,160C80,120,160,80,320,80C480,80,560,160,720,160C880,160,960,80,1120,50C1280,16,1360,80,1440,0L1440,320L0,320Z"
      ></path>
    </svg>

    <section class="bg-gray-300 flex items-center justify-center">
      <p class="text-center">{{ networking }}</p>
      <div class="w-72">
        <lottie-player src="./machine-learning.json" speed="1" autoplay loop></lottie-player>
      </div>
    </section>

    <svg viewBox="0 0 1440 200" class="fill-gray-300">
      <path d="M0,132C180,0,1360,160,1440,0L140,0L0,0Z"></path>
    </svg>

    <section class="flex items-center justify-center">
      <div class="w-72">
        <lottie-player src="./debugging.json" speed="1" autoplay loop></lottie-player>
      </div>
      <p class="text-center">{{ networking }}</p>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      networking: 'description',
    }
  },
}
</script>
