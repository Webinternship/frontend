<template>
  <div class="text-sm grid grid-cols-3 gap-2 p-4 items-center" :key="colorKey">
    <span v-for="(course, wordIndex) in courses" :key="wordIndex">
      <BgridsC>
        <template #title>
          <div>
            <h2
              :style="{
                backgroundColor: currentBgcolor,
                color: currentColor,
                padding: '10px',
              }"
            >
              <span class="animate-fade-in" :style="{ animationDelay: `${wordIndex * 0.25}s` }">
                {{ course }}
              </span>
            </h2>
            <p class="break-words whitespace-normal">{{ descriptions[wordIndex] }}</p>
          </div>
        </template>
      </BgridsC>
    </span>
  </div>
</template>

<script>
import BgridsC from './Atoms/grids.vue'

export default {
  components: { BgridsC },
  data() {
    return {
      descriptions: [
        'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequatur iste nobis vero, facilis assumenda recusandae vel. Deleniti fuga beatae provident suscipit omnis quibusdam molestiae accusantium harum magni ducimus. Fugiat, hic!',
        'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequatur iste nobis vero, facilis assumenda recusandae vel. Deleniti fuga beatae provident suscipit omnis quibusdam molestiae accusantium harum magni ducimus. Fugiat, hic!',
        'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequatur iste nobis vero, facilis assumenda recusandae vel. Deleniti fuga beatae provident suscipit omnis quibusdam molestiae accusantium harum magni ducimus. Fugiat, hic!',
        'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequatur iste nobis vero, facilis assumenda recusandae vel. Deleniti fuga beatae provident suscipit omnis quibusdam molestiae accusantium harum magni ducimus. Fugiat, hic!',
        'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequatur iste nobis vero, facilis assumenda recusandae vel. Deleniti fuga beatae provident suscipit omnis quibusdam molestiae accusantium harum magni ducimus. Fugiat, hic!',
        'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequatur iste nobis vero, facilis assumenda recusandae vel. Deleniti fuga beatae provident suscipit omnis quibusdam molestiae accusantium harum magni ducimus. Fugiat, hic!',
      ],
      colors: ['purple', 'white'], // Array of colors
      Bgcolors: ['lightblue', 'green'], // Array of colors
      colorIndex: 0,
      BgcolorIndex: 0,
    }
  },
  props: {
    courses: Array,
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
