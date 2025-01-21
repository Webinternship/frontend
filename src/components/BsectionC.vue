<template>
  <div class="flex h-64 justify-center">
    <div v-if="position === 'left'" class="mt-24 w-96 ml-16">
      {{ title }}
    </div>
    <lottie-player
      :src="lottieSrc"
      background="transparent"
      speed="1"
      autoplay
      loop
      class="w-7/12"
    />
    <div v-if="position === 'right'" class="mt-24 w-96 ml-16">
      {{ title }}
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    lottieSrc: {
      type: String,
      required: true,
    },
    backgroundColor: {
      type: String,
      default: 'transparent',
    },
    position: {
      type: String,
      default: 'left',
      validator: (value) => ['left', 'right'].includes(value)
    },
  },
};
</script>

<style scoped>
.flex {
  background-color: v-bind(backgroundColor);
}
</style>
