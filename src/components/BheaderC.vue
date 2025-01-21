<template>
  <div class="bg-white">
    <!-- Header Section -->
    <div
      class="bg-gray-200 p-3 flex items-center fixed w-full z-10 top-0 left-0 space-x-2 sm:space-x-4 md:space-x-6 lg:space-x-12 justify-between"
    >
      <!-- Logo Section -->
      <div>
        <img src="./Icons/graduate.svg" alt="Graduate Logo" class="w-8 sm:w-10 md:w-12 lg:w-14" />
      </div>

      <!-- Navigation Buttons -->
      <div class="hidden sm:flex items-center space-x-4">
        <button class="flex items-center gap-2">home</button>
        <a href="#" class="hidden sm:block">student management</a>
      </div>

      <!-- Search Bar -->
      <div class="flex-grow mx-4">
        <BsearchBar :items="courses" @itemSelected="handleItemSelected" />
      </div>

      <!-- Action Buttons -->
      <div class="flex items-center gap-2 sm:gap-4 pr-16">
        <button class="border border-blue-500 p-2 rounded-xl text-sm sm:text-base">log in</button>
        <BpulseButtonC/>
      </div>
    </div>

    <!-- SVG Bézier Curve -->

  </div>
</template>

<script>
import BpulseButtonC from './BpulseButtonC.vue';
import BsearchBar from './BsearchBar.vue'

export default {
  components: {
    BsearchBar, BpulseButtonC
  },
  data() {
    return {
      courses: [
        'Introduction to Programming',
        'Advanced JavaScript',
        'Vue.js Essentials',
        'Database Management',
        'Machine Learning Basics',
        'React for Beginners',
      ],
      selectedCourse: '',
    }
  },
  methods: {
    handleItemSelected(course) {
      this.selectedCourse = course
    },
  },
}
</script>
