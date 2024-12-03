<template>
  <div id="app">
    <Header />
    <Skills />
    <Projects />
    <Contact />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Skills from './components/Skills.vue';
import Projects from './components/Projects.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';

export default {
  components: {
    Header,
    Skills,
    Projects,
    Contact,
    Footer,
  },
};
</script>

<style>
body {
  font-family: Arial, sans-serif;
}
</style>