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
      <SectionHeading :page="pages[0]" />
    </section>
    <section :id="pages[1].title.trim()" class="jumbotron">
      <SectionHeading :page="pages[1]" />

    </section>
    <section :id="pages[2].title">
      <SectionHeading :page="pages[2]" />

    </section>
    <section :id="pages[3].title">
      <SectionHeading :page="pages[3]" />

    </section>
    <section :id="pages[4].title">
      <SectionHeading :page="pages[4]" />

    </section>
    <section :id="pages[5].title">
      <SectionHeading :page="pages[5]" />

    </section>
    <section :id="pages[6].title">
      <SectionHeading :page="pages[6]" />

    </section>


  </main>
</template>

<script>
import NavLink from './NavLink.vue';
import SectionHeading from './SectionHeading.vue';

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
    SectionHeading
  }
  // add things here


}
</script>

<style lang="scss">
@import "../styles/variables.scss";


#home {
  background-image: url(../assets/bg-9.jpg);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}

section {
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

section>* {
  height: 100%;
}

section#home {
  h3 {
    color: $second_color;
  }

}

section#about {
  background-color: $second_color;
}
section#services {
  background-color: $first_color;
}
section#process {
  background-color: rgba($fourth_color, 0.1);
}
section#numbers {
  background-image: url(../assets/bg-10.jpg);
}
section#testimonials {
  background-color: $first_color;
}
section#get {
  background-color: $second_color;
}
</style>