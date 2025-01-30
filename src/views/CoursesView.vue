<template>
  <div class="grid grid-cols-3 gap-8 p-2 h-screen" :key="colorKey">
    <span v-for="(course, courseIndex) in courses" :key="courseIndex">
      <course>
        <h2
          :style="{
            backgroundColor: currentBgcolor,
            color: currentColor,
            animationDelay: `${courseIndex * 0.25}s`,
          }"
          class="animate-fade-in p-1"
        >
          {{ course }}
        </h2>
        <template #calendar>{{ calendar[courseIndex] }}</template>
        <template #instructor>{{ instructor[courseIndex] }}</template>
        <p class="break-words whitespace-normal">{{ descriptions[courseIndex] }}</p>
      </course>
    </span>
  </div>
</template>

<script>
import course from '@/components/Atoms/course.vue'

export default {
  components: { course },
  data() {
    return {
      calendar: ['30min', '1hour', '30days'],
      instructor: ['30min', '1hour', '30days'],
      descriptions: ['lorem epsum', 'lorem epsum', 'lorem epsum', 'lorem epsum'],
      colors: ['purple', 'white'], // Array of colors
      Bgcolors: ['lightblue', 'green'], // Array of colors
      colorIndex: 0,
      BgcolorIndex: 0,
      courses: ['python', 'javascript', 'newtworking'],
    }
  },

  computed: {
    currentColor() {
      return this.colors[this.colorIndex]
    },
    currentBgcolor() {
      return this.Bgcolors[this.BgcolorIndex]
    },
    colorKey() {
      return `${this.colorIndex}`
    },
  },
  watch: {
    colorIndex(newValue) {
      if (newValue >= this.colors.length) {
        this.colorIndex = 0 // Reset to first color if we run out of colors
      }
    },
    BgcolorIndex(newValue) {
      if (newValue >= this.Bgcolors.length) {
        this.BgcolorIndex = 0 // Reset to first color if we run out of colors
      }
    },
  },
  methods: {
    changeColor() {
      this.colorIndex++
    },
    BgchangeColor() {
      this.BgcolorIndex++
    },
  },
  mounted() {
    setInterval(this.changeColor, 4000)
    setInterval(this.BgchangeColor, 4000)
  },
}
</script>

<style>
@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

.animate-fade-in {
  animation: fade-in 0.5s ease-in-out forwards;
  opacity: 0;
}
</style>
