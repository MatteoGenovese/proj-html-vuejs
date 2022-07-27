<template>
  <div id="app">
    <Header :pages="pages" :contacts="contacts" />
    <Main :pages="pages" :contacts="contacts" :cards="cards" />
    <Footer :contacts="contacts" :footerLinks="footerLinks" />
  </div>
</template>

<script>

import Main from './components/Main.vue';
import Footer from './components/Footer.vue';
import Header from './components/Header.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
    Header
  },
  data:
    function () {
      return {
        pages: [
          {
            title: 'home',
            extend_title: 'logistic services',
            highlitedSubtitle: '',
            subtitle: 'cargo transport',
            description: 'Fractional or exclusive road cargo transportation to all regions, with small, medium and large vehicles.',
            highlitedPosition:"none",
          },
          {
            title: 'about',
            extend_title: 'who we are',
            highlitedSubtitle: 'Excellence',
            subtitle: ' in Transport',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum velit tortor, interdum sed cursus eu, sagittis ut nunc. Sed vitae tellus et arcu aliquet faucibus fermentum non lacus.',
            highlitedPosition:"before",
          },
          {
            title: 'services',
            extend_title: 'road transport',
            highlitedSubtitle: 'Services',
            subtitle: 'Main ',
            description: 'With all of this expertise and capability comes an unrivalled commitment to customer service. We will work hard to understand your needs in order to develop a productive, long-term partnership.',
            highlitedPosition:"after",
          },
          {
            title: 'process',
            extend_title: 'how it works in practice',
            highlitedSubtitle: 'Logistical',
            subtitle: 'Procedure',
            description: 'We work with innovative methodologies to ensure that the entire delivery process is done from start to finish as planned.',
            highlitedPosition:"before",
          },
          {
            title: 'numbers',
            extend_title: 'what are we doing',
            highlitedSubtitle: 'Results',
            subtitle: 'in Numbers',
            description: '',
            highlitedPosition:"before",
          },
          {
            title: 'testimonials',
            extend_title: 'customer testimonials',
            highlitedSubtitle: 'Feedback',
            subtitle: 'Trusted',
            description: 'We work intensively in search of ideals that can add up in the lives of our customers. This is what moves us and we are grateful for the recognition.',
            highlitedPosition:"after",
          },

          {
            title: 'get in touch',
            extend_title: 'send a message',
            highlitedSubtitle: 'touch',
            subtitle: 'get in',
            description: 'We will respond to your message as soon as possible.',
            highlitedPosition:"after",
          },
        ],
        contacts: {
          openHours: 'Open Hours: Mon - Sat - 9:00 - 18:00',
          telephoneNumber: '+1 (305) 1234-5678',
          email: 'hello@example.com',
          address: 'Main Avenue, 987',
        },
        footerLinks: [
          {
            topic: 'About',
            links: ['The Company', 'Institutional', 'Social & Events', 'Innovation', 'Environment', 'Technology']
          },
          {
            topic: 'Transport',
            links: ['Industrialized', 'Chemicals', 'Packaged Liquids', 'Construction', 'Laminated Wood', 'And others']
          },
          {
            topic: 'Support',
            links: ['Responsibility', 'Terms of Use', 'About Cookies', 'Privacy Policy', 'Accessibility', 'Information']
          },
        ],
        cards:[{
          image_url: "",
          cardTitle: "Technology",
          cardDescription:"We are continually focused on developing technology solutions adapted to our client's needs.",
          isFeedback:false,
        },
        {
          image_url: "",
          cardTitle: "Reefer Cargo",
          cardDescription:"Regular and frequent monitoring from the receipt of the loaded container to final destination.",
          isFeedback:false,
        },
        {
          image_url: "",
          cardTitle: "Dry Cargo",
          cardDescription:"We work with most types of dry cargo, from valuable cargo to the most dangerous requiring care.",
          isFeedback:false,
        },
        {
          image_url: "logo-1.png",
          cardTitle: "",
          cardDescription:"Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque. Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
          isFeedback:true,
        },
        {
          image_url: "logo-2.png",
          cardTitle: "",
          cardDescription:"Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque. Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
          isFeedback:true,
        },

        {
          image_url: "logo-3.png",
          cardTitle: "",
          cardDescription:"Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque. Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
          isFeedback:true,
        },
        ]


      }
    },
}
</script>

<style lang="scss">
@import "./styles/variables.scss";
@import "~bootstrap/scss/bootstrap.scss";

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
