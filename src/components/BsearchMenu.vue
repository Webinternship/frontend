<template>
  <div class="flex">
    <div class="bg-gray-400 p-2">
      <h2>Menu</h2>
      <input
        type="text"
        id="mySearch"
        v-model="searchQuery"
        @input="filterMenu"
        placeholder="Search.."
        title="Type in a category"
      />
      <ul id="myMenu">
        <li v-for="(item, index) in filteredItems" :key="index" class="hover:bg-red-400">
          <a href="#">{{ item }}</a>
        </li>
      </ul>
    </div>

    <div class="bg-gray-100 w-full h-screen p-5">
      <h2 class="font-bold text-center">Page Content</h2>
      <p>
        Start to type for a specific category inside the search bar to "filter" the search options.
      </p>
      <p>
        Some text..Some text..Some text..Some text..Some text..Some text..Some text..Some text..
      </p>
      <p>
        Some other text..Some text..Some text..Some text..Some text..Some text..Some text..Some
        text..
      </p>
      <p>Some text..</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      searchQuery: '',
      menuItems: [
        'HTML',
        'CSS',
        'JavaScript',
        'PHP',
        'Python',
        'jQuery',
        'SQL',
        'Bootstrap',
        'Node.js',
      ],
    }
  },
  computed: {
    filteredItems() {
      if (this.searchQuery === '') {
        return this.menuItems
      } else {
        return this.menuItems.filter((item) =>
          item.toUpperCase().includes(this.searchQuery.toUpperCase()),
        )
      }
    },
  },
  methods: {
    // The @input event is already handled by the v-model directive
  },
}
</script>

<style>
/* ... your CSS styles ... */
</style>
