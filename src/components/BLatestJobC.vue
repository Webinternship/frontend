<template>
  <div class="text-sm grid grid-cols-3 gap-2 p-4 items-center" :key="colorKey">
    <span
      v-for="(text, wordIndex) in texts"
      :key="wordIndex"
      class="animate-fade-in"
      :style="{ animationDelay: `${wordIndex * 0.25}s` }"
    >
      <BgridsC>
        <template #title>
          <div>
          <h2
            :style="{
              backgroundColor: currentBgcolor,
              color: currentColor,
              padding: '10px',
              border: '2px ',
            }"
          >
            {{ text }}
          </h2>
          <p class="break-words whitespace-normal">{{ descriptions[wordIndex] }}</p>
        </div>
        </template>

      </BgridsC>
    </span>
  </div>
</template>
<script>
import BgridsC from '../components/BgridsC.vue'

export default {
  components: { BgridsC },
  data() {
    return {
      texts: [
        'programming',
        'debugging',
        'cybersecurity',
        'artificial intelligence',
        'data structure and algorithms',
        'networking',
      ],
      descriptions: [
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
  computed: {
    splitTexts() {
      return this.texts.map((text) => text.split(' '))
    },
    currentColor() {
      return this.colors[this.colorIndex]
    },
    currentBgcolor() {
      return this.Bgcolors[this.BgcolorIndex]
    },
    colorKey() {
      return `${this.colorIndex}`
    },
    BgcolorKey() {
      return `${this.BgcolorIndex}`
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

/* Apply animation delay to each word */
</style>
