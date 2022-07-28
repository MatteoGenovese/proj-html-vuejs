<template>
  <li v-if="page.title!='numbers' && page.title!='getintouch' ">
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

.nav-bar li{
    height: 100%;
    list-style-type: none;
    display: flex;
    align-items: center;
    &:hover{
      cursor: pointer;
    }
}

</style>