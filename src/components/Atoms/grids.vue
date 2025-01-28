<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div>
    <div class=" rounded p-4 text-center w-full h-full flex flex-col  border border-gray-200 shadow-inner" style="background: url(https://i.ibb.co/qCkd9jS/img1.jpg);">
      <slot name="title"></slot>
      <div class="grid grid-cols-3 gap-2 text-sm">
        <div :class="Style"><img src="./Icons/calendar.svg" alt="" />posted times ago</div>
        <div :class="Style"><img src="./Icons/company.svg" alt="" />?</div>
        <div :class="Style"><img src="./Icons/clock.svg" alt="" />length</div>
        <div :class="Style"><img src="./Icons/calendar.svg" alt="" />times ago</div>
        <button :class="Style" class="justify-center bg-blue-500 text-white">learn now</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      Style: 'bg-gray-300 rounded p-1 flex  gap-2 mt-4',
    }
  },
}
</script>
