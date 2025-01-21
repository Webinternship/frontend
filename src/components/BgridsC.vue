<template>
  <div>
    <div class="bg-gray-200 rounded p-4 text-center w-full h-full flex flex-col">
      <slot name="title"></slot>
      <div class="grid grid-cols-3 gap-2 text-sm">
        <div :class="infoStyle">
          <img src="./Icons/calendar.svg" alt="" class="w-4 h-4" />
        </div>
        <div :class="infoStyle">
          <img src="./Icons/company.svg" alt="" class="w-4 h-4" />
        </div>
        <div :class="infoStyle">
          <img src="./Icons/feather-clock.svg" alt="" class="w-4 h-4" />
        </div>
        <div :class="infoStyle">
          <img src="./Icons/info.svg" alt="" class="w-4 h-4" />
        </div>
        <div :class="infoStyle">
          <img src="./Icons/calendar.svg" alt="" class="w-4 h-4" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {},
  data() {
    return {
      infoStyle: 'bg-gray-300 rounded p-1 flex items-center gap-2 mt-4',
    }
  },
}
</script>
