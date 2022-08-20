<template>
  <base-layout page-title="The Details" page-default-back-link="/memories">
    <h2 v-if="!loadedMemory">Could not find a memory for the given id.</h2>
    <h2 v-else="">Load it</h2>
  </base-layout>
</template>

<script>
export default {
  data() {
    return {
      memoryId: null
    }
  },
  computed: {
    loadedMemory() {
      return this.$store.getter.memory(this.memoryId);
    }
  },
  watch: {
    '$route'(currentRoute) {
      this.memoryId = currentRoute.params.id;
    } 
  }
};
</script>