<template>
  <main>
    <section :id="pages[0].title">
      <div class="nav-bar">
        <div class="container">
          <div class="logo">
            NEXGEN
          </div>
          <div class="nav-links">
            <ul>
              <NavLink v-for="(page, index) in pages" :key="index" :page="page" />
            </ul>
          </div>
          <div>
            C
          </div>
          <div class="social">
            <button>GET IN TOUCH</button>
          </div>
        </div>
      </div>
    </section>
    <section :id="pages[1].title" class="jumbotron">

    </section>
    <section :id="pages[2].title">

    </section>
    <section :id="pages[3].title">

    </section>
    <section :id="pages[4].title">

    </section>
    <section :class="pages[5].title">

    </section>


  </main>
</template>

<script>
import NavLink from './NavLink.vue';

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
  components: {
        NavLink,
    }
  // add things here


}
</script>

<style lang="scss">
@import "../styles/variables.scss";


#home{
  background-image: url(../assets/bg-9.jpg);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  height: 700px;
}
.nav-bar {
  color: $second_color;
  height: 50px;
}

.nav-bar>* {
  height: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;

  &>* {
    height: 100%;
    display: flex;
    align-items: center;
    padding-right: 5px;
    padding-left: 5px;

    ul {
      margin-bottom: 0;
    }

    &>* {
      height: 100%;
      display: flex;
      align-items: center;
      padding-right: 5px;
      padding-left: 5px;

      &>* {
        height: 100%;
        display: flex;
        align-items: center;
        padding-right: 5px;
        padding-left: 5px;
      }
    }
  }
}

.nav-links {
  flex-grow: 1;
}

.nav-links {
  height: 100%;
  justify-content: flex-end;
}
</style>