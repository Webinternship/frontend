<template>
  <div
    class="flex items-center justify-center bg-gradient-to-r from-blue-200 to-purple-300 text-sm p-3"
  >
    <img
      src="@/components/Icons/graduate.svg"
      alt="Graduate Logo"
      class="sm:w-10 md:w-12 lg:w-14"
    />
    <p class="animate-bounce">birhan academy</p>

    <div class="hidden sm:flex items-center space-x-4 relative">
      <router-link to="/"><button class="flex items-center gap-2 ml-16">home</button></router-link>
      <router-link to="/LatestCourses">
        <span class="absolute flex ml-12">
          <span class="absolute animate-ping rounded-full size-3 bg-sky-400"></span>
          <span class="absolute size-3 rounded-full bg-sky-500"></span>
        </span>
        <button class="bg-amber-200 p-1 rounded">courses</button>
      </router-link>
      <!-- <router-link to="/teachers" class="bg-indigo-300 p-1 rounded">For Teachers</router-link> -->
    </div>

    <div class="mx-4">
      <search :items="courses" @itemSelected="handleItemSelected" />
    </div>

    <div class="flex items-center gap-2 sm:gap-4 pr-16">
      <button class="relative p-2 bg-blue-400 text-white rounded-md hover:bg-blue-600">
        <span>sign up</span>
        <span class="absolute inset-0 bg-blue-700 rounded-md opacity-50 animate-pulse"></span>
      </button>
    </div>
  </div>
</template>

<script>
import search from '@/components/Atoms/search.vue'

export default {
  components: { search },
  data() {
    return {
      courses: ['introduction to python'],
    }
  },
  methods: {
    handleItemSelected(course) {
      console.log(`Selected course: ${course}`)
    },
  },
}
</script>
