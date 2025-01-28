<template>
  <HeaderC />
  <herofirst />
  <div style="position: relative">
    <svg viewBox="0 0 1440 200" style="position: absolute; top: 0px">
      <path d="M0,132C180,0,1360,160,1440,0L140,0L0,0Z"></path>
    </svg>
  </div>
</template>

<script>
import Herofirst from './components/Atoms/herofirst.vue'
import HeaderC from './components/headerC.vue'

export default {
  components: { HeaderC, Herofirst },
}
</script>
