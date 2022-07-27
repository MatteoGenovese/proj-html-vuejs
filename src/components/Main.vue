<template>
  <main>
    <!-- Home -->
    <section :id="pages[0].title" class="d-flex flex-column">
      <div class="nav-bar d-flex">
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
            <MyButton :msg="'GET IN TOUCH'" :buttonType="'light-blue'" :link="'get in touch'" />
          </div>
        </div>
      </div>
      <div class="home d-flex align-items-center justify-content-center flex-grow-1">
        <div class="container d-flex align-items-center">
          <div class="box w-50 d-flex flex-column justify-content-center">
            <SectionHeading :page="pages[0]" />
            <div class="d-flex">
              <MyButton :msg="'GET IN TOUCH'" :buttonType="'light-blue'" :link="'get in touch'" :classBtn="'mx-3'" />
              <MyButton :msg="'READ MORE'" :buttonType="'bgc-none'" :link="'about'" />
            </div>
          </div>
        </div>
      </div>

    </section>

    <!-- about -->
    <section :id="pages[1].title.trim()" class="jumbotron d-flex flex-column">
      <div class="container d-flex flex-grow-1 align-items-center">
        <div class="w-75">
          <SectionHeading :page="pages[1]" />
          <div>
            Praesent fringilla quis massa et placerat. Mauris eu dui eget urna pellentesque gravida vitae quis nibh. Ut
            at augue tortor. Pellentesque quis suscipit magna.

            <div class="quote">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed quam tortor, ultrices
              accumsan mauris eget, pulvinar tincidunt erat. Sed nisi nisi, rutrum sit amet elit.</div>

            Sed mauris nulla, tempor eu est vel, dapibus hendrerit mauris curabitur dictum pharetra.
            <ul class="with-list-style">
              <li>Lorem ipsum dolor sit amet</li>
              <li>Consectetur adipiscing elit</li>
              <li>Integer molestie lorem at massa</li>
              <li>Facilisis in pretium nisl aliquet</li>
              <li>Dapibus hendrerit mauris curabitur</li>
            </ul>
          </div>
        </div>


        <div class="w-25">
          <div class="vehicles">
            <h4>Vehicle Types</h4>
            <div class="vehicle-row">
              <div class="vehicle-container">
                <img src="../assets/truck-1.png" alt="">
              </div>
              <div class="vehicle-information">
                <div class="vehicle-size">Light</div>
                <div class="vehicle-weight">Max Weight 1200 Kg</div>
              </div>
            </div>
            <hr>
            <div class="vehicle-row">
              <div class="vehicle-container">
                <img src="../assets/truck-1.png" alt="">
              </div>
              <div class="vehicle-information">
                <div class="vehicle-size">Medium</div>
                <div class="vehicle-weight">Max Weight 6000 Kg</div>
              </div>
            </div>
            <hr>
            <div class="vehicle-row">
              <div class="vehicle-container">
                <img src="../assets/truck-1.png" alt="">
              </div>
              <div class="vehicle-information">
                <div class="vehicle-size">Heavy</div>
                <div class="vehicle-weight">Max Weight 24000 Kg</div>
              </div>
            </div>

          </div>

          <div class="certifications">
            <h4>Certifications</h4>
            <div class="certification-row d-flex">
              <img src="../assets/certificate.png" alt="">
              <img src="../assets/certificate.png" alt="">
            </div>
          </div>





        </div>
      </div>
    </section>

    <!-- services -->
    <section :id="pages[2].title">
      <div class="container ">
        <div class="w-75">
          <SectionHeading :page="pages[2]" />
        </div>
      </div>
    </section>

    <!-- process -->
    <section :id="pages[3].title">
      <div class="container ">
        <div class="w-75">
          <SectionHeading :page="pages[3]" />
        </div>
      </div>
    </section>

    <!-- numbers -->
    <section :id="pages[4].title">
      <div class="container ">
        <div class="w-75">
          <SectionHeading :page="pages[4]" />
        </div>
      </div>
    </section>

    <!-- testimonials -->
    <section :id="pages[5].title">
      <div class="container ">
        <div class="w-75">
          <SectionHeading :page="pages[5]" />
        </div>
      </div>
    </section>

    <!-- getintouch -->
    <section :id="pages[6].title.trim()">
      <div class="container ">
        <div class="w-75">
          <SectionHeading :page="pages[6]" />
        </div>
      </div>
    </section>


  </main>
</template>

<script>
import NavLink from './NavLink.vue';
import SectionHeading from './SectionHeading.vue';
import MyButton from './MyButton.vue';

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
    SectionHeading,
    MyButton
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

main section {
  min-height: 700px;
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

      &>*:not(a) {
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

ul.with-list-style {
  padding-left: 1rem;
}

.quote {
  padding-left: 2rem;
  margin-top: 2rem;
  margin-bottom: 2rem;
  padding-top: 1rem;
  padding-bottom: 1rem;
  border-left: 5px solid rgba($sixth_color, 0.4);
  font-style: italic;
}

.vehicle-row {
  display: flex;

  .vehicle-container {
    width: 90px;
    background-color: rgba($sixth_color, 0.4);
    border-radius: 5px;
    padding: 0.25rem 0.5rem;
    margin-right: 1rem;

    img {
      width: 100%;
    }
  }
}
.vehicles,
.certifications{
  h4{
    margin-bottom: 1.5rem;
  }
}

.certifications {
  margin-top: 3rem;

  .certification-row {
    height: 150px;

    img {
      height: 120px;
      margin-right: 10px;
      box-shadow: 5px 5px 4px #dddddd;
    }
  }
}
</style>