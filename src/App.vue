<template>
  <div
    class="flex items-center justify-center bg-gradient-to-r from-blue-200 to-purple-300 text-sm p-4"
  >
    <img
      src="./components/Icons/graduate.svg"
      alt="Graduate Logo"
      class="sm:w-10 md:w-12 lg:w-14"
    />
    <p>birhan academy</p>
    <div class="hidden sm:flex items-center space-x-4">
      <router-link to="/"><button class="flex items-c enter gap-2 ml-16">home</button></router-link>
      <router-link to="/LatestCourses" class="bg-amber-200 p-1 rounded">Latest Courses</router-link>
      <!-- <router-link to="/LatestCourses" class="bg-amber-200 p-1 rounded">course management</router-link> -->
      <!-- <router-link to="/tasks">tasks</router-link> -->
    </div>

    <div class="mx-4">
      <search :items="courses" @itemSelected="handleItemSelected" />
    </div>

    <div class="flex items-center gap-2 sm:gap-4 pr-16">
      <!-- <router-link to="/Login" class="border border-gray-900 p-2 rounded">log in</router-link> -->
      <button class="relative p-2 bg-blue-400 text-white rounded-md hover:bg-blue-600">
        <span>sign up</span>
        <span
          class="absolute inset-0 bg-blue-700 rounded-md"
          style="animation: pulse 2s infinite"
        ></span>
      </button>
    </div>
  </div>
  <router-view></router-view>
  <FooterC />
</template>

<script>
import { RouterLink, RouterView } from 'vue-router'

import search from '@/components/Atoms/search.vue'
import FooterC from './components/footerC.vue'

export default {
  components: {
    RouterLink,
    RouterView,
    search,
    FooterC,
  },
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
