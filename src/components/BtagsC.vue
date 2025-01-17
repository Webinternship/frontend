<template>
  <div class="bg-gray-100 rounded-lg p-2">
    <slot></slot>
    <li class="flex pr-4 space-x-16">
      <slot name="jobs"></slot>jobs <slot name="subscribers"></slot>subscribers
    </li>
  </div>
</template>

<script>
export default {}
</script>
