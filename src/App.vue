<template>
  <BheaderC />
  <div >
    <BheroC />
  <BLatestJobC />
  <BfooterC />
  <BsearchMenu />
  </div>
</template>

<script>
import BheaderC from './components/BheaderC.vue'
import BheroC from './components/BheroC.vue'
import BLatestJobC from './components/BLatestJobC.vue'
import BfooterC from './components/BfooterC.vue'
import BsearchMenu from './components/BsearchMenu.vue'
export default {
  components: { BheaderC, BheroC, BfooterC, BLatestJobC, BsearchMenu },
}
</script>
