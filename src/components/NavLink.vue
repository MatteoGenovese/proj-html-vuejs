<template>

  <li v-if="page.title!='numbers'">
    {{page.title}}
  </li>


</template>

<script>
export default {
    name:"NavLink",
    props:{
        page: {
            type: Object,
            required: true,
        },
    },

}
</script>

<style lang="scss">

li{
    height: 100%;
    list-style-type: none;
    display: flex;
    align-items: center;
}

</style>