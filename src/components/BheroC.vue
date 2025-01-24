<template>
  <div class="flex h-screen">
    <BheroSub />
    <ul>
      <li v-for="no in 3" :key="no">
        <a href="" class="hover:ml-16">a place for ads and values</a>
      </li>
    </ul>
  </div>
</template>

<script>
import BheroSub from './BheroSub.vue'

export default {
  components: { BheroSub },
}
</script>
