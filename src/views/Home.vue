<template>
  <v-app>
    <Hero/>
    <Experience/>
    <ContactDetails/>
    <Footer/>
  </v-app>
</template>

<script>
import Hero from './components/hero';
import Experience from './components/experience';
import ContactDetails from "./components/contactDetails";
import Footer from "./components/footer";
export default {
  name: 'App',
  components: {
    Hero,
    Experience,
    ContactDetails,
    Footer
  },
};
</script>