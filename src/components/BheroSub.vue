<template>
  <div class="flex-grow overflow-y-auto bg-gradient-to-r from-yellow-200 to-blue-300">
    <div class="bg-black">
      <div class="flex justify-center height">
        <div class="relative mt-32">
          <h1
            class="absolute left-0 text-4xl sm:text-7xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-purple-400 to-pink-600 animate-slide-in-left"
          >
            welcome to the Passion Academy!
          </h1>
          <div class="absolute right-0 mr-20 animate-slide-in-right">
            <lottie-player
              src="./programmingBoy.json"
              speed="1"
              autoplay
              loop
              class="w-72"
            ></lottie-player>
          </div>
        </div>
      </div>
    </div>

    <svg viewBox="0 0 1440 200">
      <path fill="black" fill-opacity="1" d="M0,132C180,0,1360,160,1440,0L140,0L0,0Z"></path>
    </svg>
    <div class="flex items-center justify-center">
      <div><h2>hellohellohellohellohellohellohellohello</h2></div>
      <lottie-player src="./cyber.json" speed="1" autoplay loop class="w-72"></lottie-player>
    </div>
    <svg viewBox="0 0 1440 200">
      <path
        fill="lightgray"
        fill-opacity="1"
        d="M0,160C80,120,160,80,320,80C480,80,560,160,720,160C880,160,960,80,1120,50C1280,16,1360,80,1440,0L1440,320L0,320Z"
      ></path>
    </svg>
    <div class="bg-gray-300 flex items-center justify-center">
      <lottie-player
        src="./machine-learning.json"
        speed="1"
        autoplay
        loop
        class="w-72"
      ></lottie-player>
      <div>hellohellohellohellohellohellohellohellohellohellohello</div>
    </div>

    <svg viewBox="0 0 1440 200">
      <path fill="lightgray" fill-opacity="1" d="M0,132C180,0,1360,160,1440,0L140,0L0,0Z"></path>
    </svg>

    <div class="flex items-center justify-center">
      <div>hellohellohellohellohellohellohellohello</div>
      <lottie-player
        src="./debugging.json"
        speed="1"
        autoplay
        loop
        class="w-72 h-72"
      ></lottie-player>
    </div>
  </div>
</template>

<style>
.height {
  height: 500px;
}
@keyframes slideInLeft {
  0% {
    transform: translateX(-100%);
    opacity: 0;
  }
  60% {
    transform: translateX(10%);
    opacity: 1;
  }
  100% {
    transform: translateX(0);
  }
}

@keyframes slideInRight {
  0% {
    transform: translateX(100%);
    opacity: 0;
  }
  60% {
    transform: translateX(-10%);
    opacity: 1;
  }
  100% {
    transform: translateX(0);
  }
}

.animate-slide-in-left {
  animation: slideInLeft 2s ease-out;
}

.animate-slide-in-right {
  animation: slideInRight 2s ease-out;
}
</style>
