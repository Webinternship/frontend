<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <FireworksC />
  <div>
    <div
      v-for="(point, index) in points"
      :key="index"
      class="absolute bg-white rounded-full mt-24"
      :style="{
        top: point.top + 'px',
        left: point.left + 'px',
        width: point.size + 'px',
        height: point.size + 'px',
      }"
    ></div>

    <div class="absolute top-32 right-96 pr-96 animate-slide-in-left">
      <div class="absolute left-0 mt-16">
        <div class="flex items-end" :class="customstyle">
          Congratulat
          <Flame />
          <div :class="customstyle">ons!</div>
        </div>
        <div :class="customstyle">You have come to the right place! (Birhan Academy)</div>
        <button
          class="rounded bg-gray-400 pr-5 p-4 mt-8 ml-96 bg-gradient-to-r from-white to-red-200 font-bold text-green-400"
        >
          Get Started
        </button>
      </div>
    </div>
    <div class="absolute bottom-8 h-96 animate-slide-in-right left-72">
      <lottie-player src="./programmer.json" speed="1" autoplay loop></lottie-player>
    </div>
  </div>
</template>

<script>
import Flame from '@/components/Atoms/flame.vue'
import FireworksC from '@/components/Atoms/fireworks.vue'

export default {
  components: { FireworksC, Flame },
  data() {
    return {
      points: this.generatePoints(),
      customstyle:
        'text-xl sm:text-7xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-purple-400 to-red-200',
    }
  },
  methods: {
    generatePoints() {
      const randomPoints = []
      for (let i = 0; i < 40; i++) {
        randomPoints.push({
          top: Math.random() * 500, // Random value between 0 and 500
          left: Math.random() * 1000,
          size: Math.random() * 20,
        })
      }
      return randomPoints
    },
  },
}
</script>
<style>
/* General Styles */

.gradient-text {
  background-image: linear-gradient(to right, #a855f7, #ec4899);
}
.fill-black path {
  fill: black;
}
.fill-light-gray path {
  fill: lightgray;
}

/* Animations */
@keyframes slideIn {
  0% {
    transform: translateX(var(--start));
  }
  60% {
    transform: translateX(var(--mid));
  }
  100% {
    transform: translateX(0);
  }
}
.animate-slide-in-left {
  --start: -100%;
  --mid: 10%;
  animation: slideIn 2s ease-out;
}
.animate-slide-in-right {
  --start: 100%;
  --mid: -10%;
  animation: slideIn 2s ease-out;
}
</style>
