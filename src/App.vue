<template>
  <BheaderC />
  <BheroC />
  <LatestCourses />
  <BfooterC />
</template>

<script>
import BfooterC from './components/BfooterC.vue'
import BheaderC from './components/BheaderC.vue'
import BheroC from './components/BheroC.vue'
import LatestCourses from './components/LatestCourses.vue'

export default {
  components: { BheaderC, BheroC, LatestCourses, BfooterC },
  data(){
    return {
      greeting: 'hello world'
    }
  }
}
</script>
