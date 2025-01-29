<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div
    class="text-sm rounded p-4 text-center shadow-inner"
    style="background: url(https://i.ibb.co/qCkd9jS/img1.jpg)"
  >
    <slot></slot>
    <div class="grid grid-cols-3 gap-2 text-xsm mt-4">
      <div :class="Style"><img src="../Icons/calendar.svg" alt="" />times ago</div>
      <div :class="Style"><img src="../Icons/company.svg" alt="" />instructor</div>
      <div :class="Style"><img src="../Icons/clock.svg" alt="" /></div>
      <div :class="Style"><img src="../Icons/calendar.svg" alt="" />times ago</div>
      <div :class="Style" class="bg-blue-500 text-white justify-center">
        <button>learn now</button>
      </div>
    </div>
    <!-- <img src="../Icons/info.svg" alt="" class="w-4 h-4" /> -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      Style: 'bg-gray-400 rounded p-1 flex gap-2 ',
    }
  },
}
</script>
