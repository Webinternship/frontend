<template>
  <div>
    <form @submit.prevent="$emit('add', newAssignment)">
      <input type="text" v-model="newAssignment" />
      <button type="submit" class="bg-gray-500 rounded">add assignment</button>
    </form>
  </div>
</template>


<script>
export default {
  data() {
    return {
      newAssignment: ''
    }
  },
}
</script>
