<template>
  <footer>
    io sono il footer
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  props: {
    contacts: {
      type: Object,
      required: true,
    },
    footerLinks: {
      type: Array,
      required: true,
    },
  },
  // add things here

}
</script>

<style lang="scss">
</style>