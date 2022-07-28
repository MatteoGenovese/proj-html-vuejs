<template>
  <main>
    <!-- Home -->
    <section :id="pages[0].title" class="d-flex flex-column">
    <div class="back-image"></div>
      <div class="nav-bar d-flex">
        <div class="container">
          <div class="logo">
            <div class="nex">NEX</div>
            <div class="gen">GEN</div>
          </div>
          <div class="nav-links">
            <ul>
              <NavLink v-for="(page, index) in pages" :key="index" :page="page" />
            </ul>
          </div>
          <div>
            <i class="fa-regular fa-user"></i>
          </div>
          <div class="social">
            <MyButton :msg="'GET IN TOUCH'" :buttonType="'light-blue'" :link="'get in touch'" />
          </div>
        </div>
      </div>
      <div class="home d-flex align-items-center justify-content-center flex-grow-1">
        <div class="container d-flex ">
          <div class="box w-50 d-flex flex-column">
            <SectionHeading :page="pages[0]" />
            <div class="d-flex home-buttons">
              <MyButton :msg="'GET IN TOUCH'" :buttonType="'light-blue'" :link="'get in touch'"
                :classBtn="'mx-3 mt-3'" />
              <MyButton :msg="'READ MORE'" :buttonType="'bgc-none'" :link="'about'" :classBtn="'mt-3'" />
            </div>
          </div>
        </div>
      </div>

    </section>

    <!-- about -->
    <section :id="pages[1].title" class="jumbotron d-flex flex-column">
      <div class="container flex-grow-1 d-flex align-items-center">
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
    <section :id="pages[2].title" class="d-flex flex-column justify-content-center">
      <div class="container d-flex flex-column">
        <div class="w-100 d-flex">
          <div class="w-75">
            <SectionHeading :page="pages[2]" />
          </div>
          <div class="w-25 d-flex justify-content-end align-items-end pb-5">

            <MyButton :msg="'SEE ALL'" :buttonType="'bgc-none'" :link="'#'" :classBtn="'mt-3'" />
          </div>
        </div>

        <div class="w-100 d-flex justify-content-between">
          <Card v-for="(card, index) in cards" :key="index" :card="card" :need="'services'" />
        </div>

      </div>
    </section>

    <!-- process -->
    <section :id="pages[3].title" class="d-flex flex-column">
      <div class="container d-flex flex-grow-1 align-items-center">
        <div class="w-100">
          <SectionHeading :page="pages[3]" class="text-center" />
          <div class="timing-line d-flex justify-content-between">
            <div class="process-sequence d-flex flex-column align-items-center">
              <div class="process-number">01</div>
              <div class="process-title">Collection of information</div>
              <div class="process-description">Lorem ipsum dolor sit amet consectetur.</div>
            </div>
            <div class="process-sequence d-flex flex-column align-items-center">
              <div class="process-number">01</div>
              <div class="process-title">Collection of information</div>
              <div class="process-description">Lorem ipsum dolor sit amet consectetur.</div>
            </div>
            <div class="process-sequence d-flex flex-column align-items-center">
              <div class="process-number">01</div>
              <div class="process-title">Collection of information</div>
              <div class="process-description">Lorem ipsum dolor sit amet consectetur.</div>
            </div>
            <div class="process-sequence d-flex flex-column align-items-center">
              <div class="process-number">01</div>
              <div class="process-title">Collection of information</div>
              <div class="process-description">Lorem ipsum dolor sit amet consectetur.</div>
            </div>
            <div class="process-sequence d-flex flex-column align-items-center">
              <div class="process-number">01</div>
              <div class="process-title">Collection of information</div>
              <div class="process-description">Lorem ipsum dolor sit amet consectetur.</div>
            </div>

          </div>

        </div>
      </div>
    </section>

    <!-- numbers -->
    <section :id="pages[4].title" class="d-flex flex-column">
      <div class="container d-flex flex-grow-1 justify-content-center flex-column">
        <div class="w-100">
          <SectionHeading :page="pages[4]" class="text-center" />
        </div>
        <div class="w-100 d-flex justify-content-around">
          <div class="kpi">
            <div class="number">128</div>
            <div class="unity">Certifications</div>
          </div>
          <div class="kpi">
            <div class="number">230</div>
            <div class="unity">Employees</div>
          </div>
          <div class="kpi">
            <div class="number">517</div>
            <div class="unity">Customers</div>
          </div>
          <div class="kpi">
            <div class="number">94</div>
            <div class="unity">Countries Served</div>
          </div>

        </div>
      </div>
    </section>

    <!-- testimonials -->
    <section :id="pages[5].title" class="d-flex flex-column">
      <div class="container d-flex  flex-column flex-grow-1 align-items-center justify-content-center">
        <div class="w-75 d-flex flex-column align-items-center">
          <SectionHeading :page="pages[5]" class="text-center" />
        </div>
        <div class="w-100 d-flex">
          <Card v-for="(card, index) in cards" :key="index" :card="card" :need="'feedback'" />
        </div>
      </div>
    </section>

    <!-- getintouch -->
    <section :id="pages[6].title.trim()" class="d-flex flex-column">
      <div class="container d-flex flex-grow-1 align-items-center">
        <div class="w-75">
          <SectionHeading :page="pages[6]" />
          <div class="form">
            
              <div class="row">
                <div class="col"><input type="text" placeholder="Name"></div>
                <div class="col"><input type="text" placeholder="Email"></div>
              </div>
              <div class="row">
                <div class="col"><input type="text" placeholder="Phone"></div>
                <div class="col">
                  <select name="more-info" id="more-info">
                    <option value="0">more-info</option>
                    <option value="1">option1</option>
                    <option value="2">option1</option>
                    <option value="3">option1</option>
                  </select>
                </div>
              </div>
              <div class="row">
                <div class="col">
                  <input type="text" placeholder="Message">
                </div>
              </div>
              <div class="row">
                <div class="col mt-4">
                  <MyButton :msg="'GET IN TOUCH'" :buttonType="'light-blue'" :link="'get in touch'"
                 />
                </div>
              

            </div>
          </div>
        </div>
        <div class="w-25">
          <div class="corporation">
            <div class="corp-container">
              <div class="corp-information">
                <div class="corp-title"> <h4>Example Inc.</h4> </div>
                <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. </div>
                <div>Praesent diam lacus, dapibus sed imperdiet consectetur.</div>
                <div class="corporation-contacts">
                  <div class="phone-number d-flex">
                    <div class="corp-icon mx-2"><i class="fa-solid fa-phone"></i></div>{{ contacts.telephoneNumber }}</div>
                  <div class="email d-flex">
                    <div class="corp-icon mx-2"><i class="fa-solid fa-envelope"></i> </div>
                    
                    {{ contacts.email }}</div>
                  <div class="address d-flex">
                    <div class="corp-icon mx-2"><i class="fa-solid fa-location-dot"></i></div>
                    
                    {{ contacts.address }}</div>
                </div>
                <div class="light-blue-color">
                <MyButton :msg="'VIEW MAP'" :buttonType="'light-blue-colors'" :link="'#'" class="mt-3" />
                </div>


              </div>
            </div>

          </div>
        </div>
      </div>
    </section>


  </main>
</template>

<script>
import NavLink from './NavLink.vue';
import SectionHeading from './SectionHeading.vue';
import Card from './Card.vue';
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
    Card,
    MyButton
}
  // add things here


}
</script>

<style lang="scss">
@import "../styles/variables.scss";


#home {

}

main section {
  min-height: 980px;
}

section#home,
.back-image {
  min-height: 976px;
}
.back-image{
  position: absolute;
  background-image: url(../assets/bg-9.jpg);
  filter: brightness(0.4);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  top:50px;
  width: 100%;
  z-index: -1;
}

section#about {
  min-height: 1000px;
}

section#services {
  min-height: 940px;
}

section#process {
  min-height: 810px;
}

section#numbers {
  min-height: 660px;
  background-image: url(../assets/bg-10.jpg);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}

section#testimonials {
  min-height: 870px;
}

section#getintouch {
  min-height: 950px;
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
  margin-top: 1.2rem;
  font-size: 1.4rem;
  text-transform: uppercase;


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
.certifications,
.corporation {
  h4 {
    margin-bottom: 1.5rem;
    color: $first_color;
  }
}

div.vehicle-size {
  color: $first_color;
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

div.home-buttons {
  margin-left: -1rem;
}

div.timing-line {
  border-top: 5px solid rgba($sixth_color, 0.5);

  div.process-title {
    font-size: 1.8rem;
    font-weight: 800;
    color: $first_color  !important;
  }

}

div.process-sequence {
  position: relative;
  top: -1.7rem;
  width: calc(100% / 5);

  &>* {
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .process-number {
    width: 50px;
    height: 50px;
    font-weight: 700;
    background-color: rgba($sixth_color, 1);
    color: $fourth_color  !important;
    border-radius: 50%;
  }
}

.kpi {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  .number {
    color: $sixth_color;
    font-size: 1.8rem;
    font-weight: 700;
  }

  .unity {
    color: $second_color;
    font-weight: 600;

  }
}

div.corp-title {
  color: $first_color  !important;
}


.corp-container {
  
  padding: 0.25rem 0.5rem;
  margin-right: 1rem;
}

div.vehicle-size {
  color: $first_color;
}

.light-blue-color{
  padding-top: 1rem;
}

div.corporation-contacts > *{
  color: $fourth_color !important;
  padding-top: 0.5rem;
  padding-bottom: 0.5rem;
}
div.corp-information > *{
    padding-top: 0.5rem;
  padding-bottom: 0.5rem;
}

.form{
  margin-right: 3rem;
}

.form input,
section#getintouch .form select{
  background-color: rgba($fifth_color, 0.5);
  padding: .5rem 1rem;
  border: 0;
  margin-top:1rem;
  border-radius: 5px;
  width: 100%;
  height: 50px;
  color: $third_color;

  option{
    color: $third_color;
  }
}
.logo .nex{
  height: 40px;
  background-color: rgba($fourth_color, 0.7);
  padding-left: 1.5rem;
  border-radius: 20px 0 0 20px;
}

.corp-icon{
    background-color: $sixth_color;
    width: 3rem;
    height: 3rem;
    display: flex;
    justify-content: center;
    align-items: center ;
    border-radius: 50%;
    i{
      color: $fourth_color;
    }
}
</style>