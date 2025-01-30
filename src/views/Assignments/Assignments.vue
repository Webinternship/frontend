<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="flex flex-col md:flex-row h-screen">
    <assignmentList :assignments="inProgress" />

    <div class="w-full md:w-1/2 bg-gray-100 shadow-md overflow-y-auto"></div>

    <assignmentList :assignments="completed" />
  </div>
</template>

<script>
// import aAssignmentCreate from './AssignmentCreate.vue'
import assignmentList from './AssignmentList.vue'

export default {
  components: { assignmentList },
  data() {
    return {
      assignments: [
        { name: 'assignment one', complete: false, id: 1, tag: 'science' },
        { name: 'assignment two', complete: false, id: 2, tag: 'math' },
        { name: 'assignment three', complete: false, id: 3, tag: 'science' },
      ],
    }
  },
  computed: {
    inProgress() {
      return this.assignments.filter((a) => a.complete === false)
    },
    completed() {
      return this.assignments.filter((a) => a.complete === true)
    },
  },

  // methods: {
  //   add(name) {
  //     this.assignments.push({
  //       name: name,
  //       complete: false,
  //       id: this.assignments.length + 1,
  //     })
  //   },
  // },
}
</script>
