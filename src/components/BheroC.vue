<template>
  <div class="bg-gradient-to-r from-yellow-100 to-green-400">
    <div class="bg-black flex justify-center">
      <div class="bg-black flex relative items-center justify-center custom-height">
        <h1
          class="absolute left-0 text-4xl sm:text-7xl font-bold text-transparent bg-clip-text gradient-text animate-slide-in-left"
        >
          Welcome to Geez Academy!
        </h1>
        <div class="absolute right-0 mr-20 animate-slide-in-right">
          <lottie-player
            src="./programmingBoy.json"
            speed="1"
            autoplay
            loop
            class="w-72 items-center"
          ></lottie-player>
        </div>
      </div>
    </div>

    <!-- SVG Separator -->
    <svg viewBox="0 0 1440 200" class="fill-black">
      <path d="M0,132C180,0,1360,160,1440,0L140,0L0,0Z"></path>
    </svg>

    <!-- Section 1 -->
    <section class="flex items-center justify-center">
      <h2 class="text-center">hellohellohellohellohellohellohellohello</h2>
      <lottie-player src="./cyber.json" speed="1" autoplay loop class="w-72"></lottie-player>
    </section>

    <!-- SVG Separator -->
    <svg viewBox="0 0 1440 200" class="fill-light-gray">
      <path
        d="M0,160C80,120,160,80,320,80C480,80,560,160,720,160C880,160,960,80,1120,50C1280,16,1360,80,1440,0L1440,320L0,320Z"
      ></path>
    </svg>

    <!-- Section 2 -->
    <section class="bg-gray-300 flex items-center justify-center">
      <lottie-player
        src="./machine-learning.json"
        speed="1"
        autoplay
        loop
        class="w-72"
      ></lottie-player>
      <p class="text-center">hellohellohellohellohellohellohellohellohellohellohello</p>
    </section>

    <!-- SVG Separator -->
    <svg viewBox="0 0 1440 200" class="fill-light-gray">
      <path d="M0,132C180,0,1360,160,1440,0L140,0L0,0Z"></path>
    </svg>

    <!-- Section 3 -->
    <section class="flex items-center justify-center">
      <p class="text-center">hellohellohellohellohellohellohellohellohellohello</p>
      <lottie-player
        src="./debugging.json"
        speed="1"
        autoplay
        loop
        class="w-72 h-72"
      ></lottie-player>
    </section>
  </div>
</template>

<style>
/* General Styles */
.custom-height {
  height: 500px;
}
.gradient-text {
  background-image: linear-gradient(to right, #a855f7, #ec4899);
}
.fill-black path {
  fill: black;
  fill-opacity: 1;
}
.fill-light-gray path {
  fill: lightgray;
  fill-opacity: 1;
}

/* Animations */
@keyframes slideIn {
  0% {
    transform: translateX(var(--start));
    opacity: 0;
  }
  60% {
    transform: translateX(var(--mid));
    opacity: 1;
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
