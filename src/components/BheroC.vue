<template>
  <div class="flex h-72 justify-content items-center">
    <lottie-player
      src="./programmingBoy.json"
      background="transparent"
      speed="1"
      autoplay
      loop
      class="w-7/12"
    ></lottie-player>
    <div class="w-6/12 mt-24 ml-auto pr-16">
      <h2 class="font-bold text-4xl">
        we devote to create <span class="text-purple-600">proficient</span> and
        <span class="text-purple-600">remarkable</span> computer science students.
      </h2>

      <button class="bg-blue-500 p-4 rounded-xl font-bold mt-4 text-white text-lg pl-16 pr-16">
        sign up to learn
      </button>
    </div>
  </div>
  <div class="flex h-72 justify-content items-center mt-16">
    <div class="mt-24 pr-32 w-128 ml-16">
      <h2 class="font-bold text-4xl">
        learn <span class="text-purple-600">debugging ( ፀረ ሓሰኻ)</span>
      </h2>
    </div>

    <lottie-player
      src="./debugging.json"
      background="transparent"
      speed="1"
      autoplay
      loop
      class="w-7/12"
    ></lottie-player>
  </div>

  <div class="flex h-72 justify-content mt-16">
    <lottie-player
      src="./cyber.json"
      background="transparent"
      speed="1"
      autoplay
      loop
      class="w-7/12"
    ></lottie-player>
    <div class="w-6/12 mt-24 ml-auto pr-32 w-16">
      <h2 class="font-bold text-4xl">
        make <span class="text-purple-600">privacy</span> and
        <span class="text-purple-600">security</span> the essence of software development
      </h2>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      about:
        'web frontend, mobile app, backend, database, fullstack, ui/ux & product design, project management, scrum master etc',
    }
  },
}
</script>
