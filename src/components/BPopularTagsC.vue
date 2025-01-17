<template>
  <div class="grid grid-cols-3 gap-4 p-4">
    <TagsC>
      <h2 class="font-bold">python</h2>
      <template v-slot:jobs>23</template>
      <template v-slot:subscribers>400</template>
    </TagsC>
    <TagsC>
      <h2 class="font-bold">python</h2>
      <template v-slot:jobs>23</template>
      <template v-slot:subscribers>400</template>
    </TagsC>
    <TagsC>
      <h2 class="font-bold">golang</h2>
      <template v-slot:jobs>23</template>
      <template v-slot:subscribers>400</template>
    </TagsC>
    <TagsC>
      <h2 class="font-bold">flutter</h2>
      <template v-slot:jobs>23</template>
      <template v-slot:subscribers>400</template>
    </TagsC>
    <TagsC>
      <h2 class="font-bold">react</h2>
      <template v-slot:jobs>23</template>
      <template v-slot:subscribers>400</template>
    </TagsC>
    <TagsC>
      <h2 class="font-bold">svelte</h2>
      <template v-slot:jobs>23</template>
      <template v-slot:subscribers>400</template>
    </TagsC>
  </div>
</template>

<script>
import TagsC from './BtagsC.vue'

export default {
  components: { TagsC },
}
</script>
