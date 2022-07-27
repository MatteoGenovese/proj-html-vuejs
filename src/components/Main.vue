<template>
  <main>
    io sono il main
  </main>
</template>

<script>
export default {
  name: 'Main',
  props: {
    pages: {
      type: Array,
      required: true,
    },
    contacts: {
      type: Object,
      required: true,
    },
    cards: {
      type: Array,
      required: true,
    },
  },
  // add things here


}
</script>

<style lang="scss">
</style>