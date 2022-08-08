<template>
  <main>
    <!-- Home -->
    <section id="home" class="d-flex flex-column">
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
              <MyButton :msg="'GET IN TOUCH'" :buttonType="'light-blue'" :link="'get in touch'" :classBtn="'mx-3'" />
              <MyButton :msg="'READ MORE'" :buttonType="'bgc-none'" :link="'about'" />
            </div>
          </div>
        </div>
      </div>

    </section>

    <!-- about -->
    <section id="about" class="jumbotron d-flex flex-column">
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
              <div class="vehicle-container d-flex align-items-center">
                <img src="../assets/truck-1.png" alt="">
              </div>
              <div class="vehicle-information">
                <div class="vehicle-size">Light</div>
                <div class="vehicle-weight">Max Weight 1200 Kg</div>
              </div>
            </div>
            <hr>
            <div class="vehicle-row">
              <div class="vehicle-container d-flex align-items-center">
                <img src="../assets/truck-1.png" alt="">
              </div>
              <div class="vehicle-information">
                <div class="vehicle-size">Medium</div>
                <div class="vehicle-weight">Max Weight 6000 Kg</div>
              </div>
            </div>
            <hr>
            <div class="vehicle-row">
              <div class="vehicle-container d-flex align-items-center">
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
            <div class="certification-row d-flex flex-wrap">
              <img src="../assets/certificate.png" alt="" class="m-2">
              <img src="../assets/certificate.png" alt="" class="m-2">
            </div>
          </div>





        </div>
      </div>
    </section>

    <!-- services -->
    <section id="services" class="d-flex flex-column justify-content-center">
      <div class="container d-flex flex-column">
        <div class="w-100 d-flex">
          <div class="w-75">
            <SectionHeading :page="pages[2]" />
          </div>
          <div class="w-25 d-flex justify-content-end align-items-end pb-5">

            <MyButton :msg="'SEE ALL'" :buttonType="'bgc-none'" :link="'#'" />
          </div>
        </div>

        <div class="w-100 d-flex justify-content-between">
          <Card v-for="(card, index) in cards" :key="index" :card="card" :need="'services'" />
        </div>

      </div>
    </section>

    <!-- process -->
    <section id="process" class="d-flex flex-column">
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
    <section id="numbers" class="d-flex flex-column">
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
    <section id="testimonials" class="d-flex flex-column">
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
    <section id="getintouch" class="d-flex flex-column">
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
              <div class="col-3 mt-4">
                <MyButton :msg="'GET IN TOUCH'" :buttonType="'light-blue'" :link="'getintouch'" />
              </div>


            </div>
          </div>
        </div>
        <div class="w-25">
          <div class="corporation">
            <div class="corp-container">
              <div class="corp-information">
                <div class="corp-title">
                  <h4>Example Inc.</h4>
                </div>
                <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. </div>
                <div>Praesent diam lacus, dapibus sed imperdiet consectetur.</div>
                <div class="corporation-contacts">
                  <div class="phone-number d-flex">
                    <div class="corp-icon mx-2"><i class="fa-solid fa-phone"></i></div>
                    <div>{{ contacts.telephoneNumber }}</div>
                  </div>
                  <div class="email d-flex">
                    <div class="corp-icon mx-2"><i class="fa-solid fa-envelope"></i> </div>
                    <div>{{ contacts.email }}</div>
                  </div>
                  <div class="address d-flex">
                    <div class="corp-icon mx-2"><i class="fa-solid fa-location-dot"></i></div>
                    <div>{{ contacts.address }}</div>
                  </div>
                </div>
                <div class="row">
                  <div class="col-7 mt-4">
                    <MyButton :msg="'VIEW MAP'" :buttonType="'light-blue-colors'" :link="'#'" />
                  </div>
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
  min-height: 61.25rem;
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url(../assets/bg-9.jpg);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  clip-path: polygon(0% 0%, 100% 0%, 100% 50%, 75% 100%, 0% 100%);

  .logo {
    .gen {
      display: flex;
      align-items: center;
      vertical-align: middle;
    }

    .nex {
      display: flex;
      align-items: center;
      height: 4rem;
      background-color: rgba($fourth_color, 0.7);
      padding-left: 2.5rem;
      border-radius: 2rem 0 0 2rem;
    }
  }

  h3 {
    color: $second_color;
  }

  .nav-bar {
    color: $second_color;
    height: 3rem;

    li {
      height: 100%;
      list-style-type: none;
      display: flex;
      align-items: center;
      padding: 0rem .5rem;
      border-radius: .5rem;
    }

    .nav-links {
      flex-grow: 1;
      height: 100%;
      justify-content: flex-end;
    }

    &>* {
      height: 100%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 2rem;
      font-size: 1.375rem;
      text-transform: uppercase;

      &>* {
        height: 100%;
        display: flex;
        align-items: center;
        padding-right: .5rem;
        padding-left: .5rem;

        ul {
          margin-bottom: 0;
        }

        &>* {
          height: 100%;
          display: flex;
          align-items: center;
          padding-right: .5rem;
          padding-left: .5rem;

          &>*:not(a) {
            height: 100%;
            display: flex;
            align-items: center;
            padding-right: .5rem;
            padding-left: .5rem;
          }
        }
      }
    }
  }
  .home-buttons {
    margin-left: -1.5rem;
  }
}

#about {
  background-color: $second_color;
  .vehicle-row {
    display: flex;
    .vehicle-size {
      color: $first_color;
    }
    .vehicle-container {
      width: 9rem;
      background-color: rgba($sixth_color, 0.4);
      border-radius: .5rem;
      padding: 0.5rem 1rem;
      margin-right: 1.5rem;
      img {
        width: 100%;
      }
    }
  }
  ul.with-list-style {
    padding-left: 1.5rem;
  }
  .quote {
    padding-left: 3rem;
    margin-top: 3rem;
    margin-bottom: 3rem;
    padding-top: 1.5rem;
    padding-bottom: 1.5rem;
    border-left: 5px solid rgba($sixth_color, 0.4);
    font-style: italic;
  }
  .certifications {
    margin-top: 5rem;
    .certification-row {
      height: 12rem;
      img {
        height: 7rem;
        margin-right: 1rem;
        box-shadow: .5rem .5rem .4rem #dddddd;
      }
    }
  }
}

#services {
  background-color: $first_color;
}
#process {
  background-color: rgba($fourth_color, 0.1);
  .timing-line {
    border-top: .5rem solid rgba($sixth_color, 0.5);
    .process-title {
      font-size: 1.875rem;
      font-weight: 800;
      color: $first_color  !important;
    }
  }
  .process-sequence {
    position: relative;
    top: -2.7rem;
    width: calc(100% / 5);
    &>* {
      text-align: center;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .process-number {
      width: 5rem;
      height: 5rem;
      font-weight: 700;
      background-color: rgba($sixth_color, 1);
      color: $fourth_color  !important;
      border-radius: 50%;
    }
  }
}

#numbers {
  background-image: url(../assets/bg-10.jpg);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  .kpi {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    .number {
      color: $sixth_color;
      font-size: 1.875rem;
      font-weight: 700;
    }
    .unity {
      color: $second_color;
      font-weight: 600;
    }
  }
}

#testimonials {
  background-color: $first_color;
}

#getintouch {
  background-color: $second_color;
  .corp-icon {
    background-color: $sixth_color;
    min-width: 5rem;
    height: 5rem;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 50%;
    .light-blue-color {
      padding-top: 1.5rem;
    }
    i {
      color: $fourth_color;
    }
  }
  .form {
    margin-right: 5rem;
    input,
    select {
      background-color: rgba($fifth_color, 0.5);
      padding: 1rem 1.5rem;
      border: 0;
      margin-top: 1.5rem;
      border-radius: .5rem;
      width: 100%;
      height: 5rem;
      color: $third_color;
    }
  }



  .corp-container {
    padding: 0.5rem 1rem;
    margin-right: 1.5rem;
    .corp-title {
      color: $first_color  !important;
    }
    .corp-information>* {
      padding-top: 1rem;
      padding-bottom: 1rem;
    }
    .corporation-contacts>* {
      color: $fourth_color  !important;
      padding-top: 1rem;
      padding-bottom: 1rem;
      &>* {
        display: flex;
        align-items: center;
      }
      .phone-number {
        display: flex;
        align-items: center;

        &>* {
          display: flex;
          align-items: center;
        }
      }
    }
  }
}

main section {
  min-height: 60rem;
  &>* {
    height: 100%;
  }
}

.vehicles,
.certifications,
.corporation {
  h4 {
    margin-bottom: 3.2rem;
    color: $first_color;
  }
}


</style>