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
    &:hover{
      cursor: pointer;
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
    }
    &:active{
      box-shadow: 0 5px 10px rgba(0, 0, 0, 0.3);
    }
}


</style>