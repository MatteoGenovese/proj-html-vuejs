<template>
  <footer class="d-flex flex-column h-100 align-content-center">
    <div class="flex-grow-1 d-flex align-content-center justify-content-center">
      <div class="container flex-grow-1 d-flex align-items-center">

        <div class="w-25 flex-column corp-info">
          <div class="logo d-flex">
            <div class="nex">NEX</div>
            <div class="gen">GEN</div>
          </div>
          <div>Functional HTML Template for Corporate & Business.</div>
          <div><i class="fa-solid fa-phone"></i> {{ contacts.telephoneNumber }}</div>
          <div><i class="fa-solid fa-envelope"></i> {{ contacts.email }}</div>
          <div><i class="fa-solid fa-location-dot"></i>{{ contacts.address }}</div>
          <div class="mt-4">
          <MyButton :msg="'GET IN TOUCH'" :buttonType="'bgc-none'" :link="'getintouch'" />
          </div>

        </div>

        <div class="w-75 d-flex">
          <Card v-for="(link, index) in footerLinks" :key="index" :card="link" :need="'links'" />
        </div>



      </div>
    </div>
  </footer>
</template>

<script>
import Card from './Card.vue';
import MyButton from './MyButton.vue';

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
  components: {
    Card,
    MyButton
  }
  // add things here

}
</script>

<style lang="scss">
@import "../styles/variables.scss";

footer {
  background-color: $first_color;
  min-height: 610px;
  color: $second_color;

  .logo .nex {
    height: 40px;
    background-color: rgba($fourth_color, 0.7);
    padding-left: 1.5rem;
    border-radius: 20px 0 0 20px;
  }

  .logo .gen {
    height: 40px;
    color: $second_color;
  }

  .logo>* {
    padding-right: 5px;
    padding-left: 5px;
  }
}

.corp-info > *{
  margin-top: 1rem;
}
</style>