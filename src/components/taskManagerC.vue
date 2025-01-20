<template>
  <div class="p-6 max-w-4xl mx-auto">
    <h1 class="text-2xl font-bold mb-4">Assignment Tracker</h1>

    <!-- Add New Assignment -->
    <div class="mb-6">
      <input
        v-model="newAssignment.title"
        type="text"
        placeholder="New Assignment"
        class="border rounded px-3 py-2 mr-2"
      />
      <input
        v-model="newAssignment.tag"
        type="text"
        placeholder="Tag"
        class="border rounded px-3 py-2 mr-2"
      />
      <button
        @click="addAssignment"
        class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600"
      >
        Add Assignment
      </button>
    </div>

    <!-- Tags -->
    <div class="mb-4">
      <h2 class="font-semibold mb-2">Filter by Tags:</h2>
      <button
        v-for="tag in uniqueTags"
        :key="tag"
        @click="filterByTag(tag)"
        class="px-3 py-1 bg-gray-200 text-gray-700 rounded-full mr-2 mb-2 hover:bg-gray-300"
      >
        {{ tag }}
      </button>
      <button
        @click="resetFilter"
        class="px-3 py-1 bg-red-500 text-white rounded-full hover:bg-red-600"
      >
        Clear Filter
      </button>
    </div>

    <!-- Assignment List -->
    <ul>
      <li
        v-for="assignment in filteredAssignments"
        class="flex justify-between items-center mb-3"
        :key="assignment.id"
      >
        <div>
          <input
            type="checkbox"
            v-model="assignment.completed"
            class="mr-2"
          />
          <span :class="{'line-through text-gray-500': assignment.completed}">
            {{ assignment.title }}
          </span>
          <span class="ml-2 px-2 py-1 text-sm bg-gray-200 text-gray-700 rounded">
            {{ assignment.tag }}
        :key="assignment.id"
          </span>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newAssignment: {
        title: "",
        tag: "",
      },
      assignments: [
        { id: 1, title: "Math Homework", completed: false, tag: "Math" },
        { id: 2, title: "Science Project", completed: false, tag: "Science" },
        { id: 3, title: "History Essay", completed: true, tag: "History" },
      ],
      filterTag: null,
    };
  },
  computed: {
    filteredAssignments() {
      if (this.filterTag) {
        return this.assignments.filter(
          (assignment) => assignment.tag === this.filterTag
        );
      }
      return this.assignments;
    },
    uniqueTags() {
      return [...new Set(this.assignments.map((a) => a.tag))];
    },
  },
  methods: {
    addAssignment() {
      if (this.newAssignment.title && this.newAssignment.tag) {
        this.assignments.push({
          id: Date.now(),
          title: this.newAssignment.title,
          completed: false,
          tag: this.newAssignment.tag,
        });
        this.newAssignment.title = "";
        this.newAssignment.tag = "";
      }
    },
    filterByTag(tag) {
      this.filterTag = tag;
    },
    resetFilter() {
      this.filterTag = null;
    },
  },
};
</script>
