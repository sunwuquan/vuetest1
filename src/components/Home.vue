<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
    <!--<router-view/>-->
    <Header :message="parentMag"></Header>
    <Section></Section>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from './Header.vue'
import Section from './Section.vue'
import Footer from './Footer.vue'

export default {
  name: 'Home',
  data () {
    return {
      flag: 1,
      parentMag: 'a message form parent'
    }
  },
  components: {Header, Section, Footer}
}
</script>
<style>
</style>
