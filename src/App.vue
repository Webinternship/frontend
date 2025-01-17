<template>
  <BheaderC />
  <BheroC />
  <!-- <taskManagerC/> -->
  <BLatestJobC />
  <BfooterC />
</template>

<script>
import BheaderC from './components/BheaderC.vue'
import BheroC from './components/BheroC.vue'
import BLatestJobC from './components/BLatestJobC.vue'
import BfooterC from './components/BfooterC.vue'

export default {
  components: { BheaderC, BheroC, BLatestJobC, BfooterC },
}
</script>
