<template>

  <div
    class="flex items-center justify-center bg-gradient-to-r from-blue-200 to-purple-300 text-sm p-4"
  >
    <img src="./Icons/graduate.svg" alt="Graduate Logo" class="sm:w-10 md:w-12 lg:w-14 mr-32" />

    <div class="hidden sm:flex items-center space-x-4">
      <button class="flex items-center gap-2">home</button>
      <a href="#" class="hidden sm:block border border-gray-500 p-2 rounded">course management</a>
    </div>

    <div class="mx-4">
      <BsearchBar :items="courses" @itemSelected="handleItemSelected" />
    </div>

    <div class="flex items-center gap-2 sm:gap-4 pr-16">
      <button class="border border-blue-500 px-2 rounded-md sm:text-base p-1">log in</button>
      <button class="relative p-2 bg-blue-400 text-white rounded-md hover:bg-blue-800">
        <span>sign up</span>
        <span
          class="absolute inset-0 bg-blue-700 rounded-md"
          style="animation: pulse 2s infinite"
        ></span>
      </button>
    </div>
  </div>

  </template>

<script>
import BsearchBar from './BsearchBar.vue'

export default {
  components: {
    BsearchBar,
  },
  data() {
    return {
      courses: [],
    }
  },
  methods: {
    handleItemSelected(course) {
      console.log(`Selected course: ${course}`)
    },
  },
}
</script>

<style>
@keyframes pulse {
  0% {
    transform: scale(1);
    opacity: 0.7;
  }
  100% {
    transform: scale(2);
    opacity: 0;
  }
}




</style>
