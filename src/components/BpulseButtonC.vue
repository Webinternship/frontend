<template>
  <button class="relative p-3 bg-blue-500 text-white rounded-md hover:bg-blue-800">
    <span>sign up</span>
    <span
      class="absolute inset-0 bg-blue-600 rounded-md"
      style="animation: pulse 2s infinite"
    ></span>
  </button>
</template>

<script>
export default {
  props: {},
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
