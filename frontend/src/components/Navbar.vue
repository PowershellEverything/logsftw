<template>
  <nav class="flex justify-between items-center mb-4">
    <span class="mr-4">
      <SearchBox @searched="updateResults" :page="page"/>
    </span>
    <h1 class="text-2xl text-gray-500 tracking-wider">LogsFTW</h1>
  </nav>
</template>

<script>
import SearchBox from './SearchBox';

export default {
  props: ['page'],
  components: {
    SearchBox
  },
  methods: {
    updateResults(results) {
      this.$emit('searched', results);
    }
  }
}
</script>