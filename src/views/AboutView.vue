<template>
  <div class="about p-6 text-center">
    <h2 class="text-3xl font-bold text-gray-800">About Us</h2>
    <p class="text-lg text-gray-600 mt-4">
      This is the About page. Here you can learn more about the app and its purpose.
    </p>
  </div>
</template>

<script>
export default {
  name: 'AboutView',
}
</script>

<style scoped>
.about {
  background-color: #f3f4f6;
  min-height: 80vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
