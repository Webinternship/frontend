<template>
  <div>
    <div class="bg-gray-100 rounded p-4 text-center w-full h-full flex flex-col">
      <slot name="title"></slot>
      <div class="grid grid-cols-3 gap-2 text-sm">
        <div :class="Style"><img src="./Icons/calendar.svg" alt="" />posted times ago</div>
        <div :class="Style"><img src="./Icons/company.svg" alt="" />?</div>
        <div :class="Style"><img src="./Icons/clock.svg" alt="" />length</div>
        <div :class="Style"><img src="./Icons/calendar.svg" alt="" />times ago</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {},
  data() {
    return {
      Style: 'bg-gray-300 rounded p-1 flex items-center gap-2 mt-4',
    }
  },
}
</script>
