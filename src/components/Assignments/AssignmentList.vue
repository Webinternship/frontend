<template>
  <section v-if="assignments.length" class="bg-gray-500 p-4 w-64">
    <h2 class="font-bold">{{ title }}</h2>

    <div class="flex gap-2">
      <button
        v-for="tag in tags"
        :key="tag"
        class="border rounded-lg p-2 py-px"
        @click="currentTag = tag"
      >
        {{ tag }}
      </button>
    </div>
    <ul>
      <label>
        <li
          v-for="assignment in filteredAssignments"
          :key="assignment.id"
          class="flex items-center justify-between"
        >
          {{ assignment.name }}
          <input type="checkbox" v-model="assignment.complete" />
        </li>
      </label>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      currentTag: 'all',
    }
  },
  props: {
    assignments: Array,
    title: String,
  },
  computed: {
    filteredAssignments() {
      if (this.currentTag === 'all') {
        return this.assignments
      }
      return this.assignments.filter((a) => a.tag === this.currentTag)
    },
    tags() {
      return ['all', ...new Set(this.assignments.map((a) => a.tag))]
    },
  },
}
</script>
