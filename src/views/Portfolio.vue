<template>
  <v-app>
    <Project/>
    <Talks/>
    <Footer/>
  </v-app>
</template>

<script>
import Footer from "./components/footer";
import Project from "./components/projects";
import Talks from "./components/workshops";
export default {
  name: 'App',
  components: {
    Project,
    Talks,
    Footer
  },
};
</script>