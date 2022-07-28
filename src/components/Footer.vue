<template>
  <footer>
              <div class="logo">
            <div class="nex">NEX</div>
            <div class="gen">GEN</div>
          </div>
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
@import "../styles/variables.scss";

footer{
  background-color: red;
  min-height: 700px;
}
.logo .nex{
  height: 40px;
  background-color: rgba($fourth_color, 0.7);
  padding-left: 1.5rem;
  border-radius: 20px 0 0 20px;
}
</style>