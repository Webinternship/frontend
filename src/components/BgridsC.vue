<template>
  <div>
    <div class="bg-gray-200 rounded p-4 text-center w-full h-full flex flex-col ">
      <slot></slot>
      <div class="grid grid-cols-3 gap-2 text-sm">
        <div :class="infoStyle">
          <img src="./Icons/calendar.svg" alt="" class="w-4 h-4" />
          <slot name="time"></slot>
          <h2 class="postTime">times ago</h2>
        </div>
        <div :class="infoStyle">
          <img src="./Icons/company.svg" alt="" class="w-4 h-4" />
          <slot name="companyName"></slot>
        </div>
        <div :class="infoStyle">
          <img src="./Icons/feather-clock.svg" alt="" class="w-4 h-4" />
          <slot name="duration"></slot>-Time
        </div>
        <div :class="infoStyle">
          <img src="./Icons/calendar.svg" alt="" class="w-4 h-4" />
          <slot name="skill"></slot>
        </div>
        <div :class="infoStyle">
          <img src="./Icons/company.svg" alt="" class="w-4 h-4" />
          <slot name="wage"></slot>/hr
        </div>
        <button class="bg-purple-600 rounded text-white h-8 mt-4">Apply</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      infoStyle: 'bg-gray-300 rounded p-1 flex items-center gap-2 mt-4'
    }
  },
}
</script>
