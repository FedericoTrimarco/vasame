<template>
  <div id="app">
    <Header :mainArray="section"/>

    <main>
      <SectionOne class="d-none d-lg-block"/>
      <SectionTwo />
      <SectionThree :mainArray="vases"/>
      <SectionFour />
    </main>

    <Footer />
  </div>
</template>

<script>
// COMPONENTS
import Header from '@/components/Header.vue'
import SectionOne from '@/components/SectionOne.vue'
import SectionTwo from '@/components/SectionTwo.vue'
import SectionThree from '@/components/SectionThree.vue'
import SectionFour from '@/components/SectionFour.vue'
import Footer from '@/components/Footer.vue'

// ARRAY
import {vases} from '@/data/allArray'
import {section} from '@/data/allArray'

export default {
  name: 'App',
  components: {
    Header,
    SectionOne,
    SectionTwo,
    SectionThree,
    SectionFour,
    Footer,
  },
  data() {
      return{
      // ARRAY
      vases,
      section,

    }
  },
}
</script>

<style lang="scss">
@import './style/variables.scss';
@import './style/utilities.scss';

  #app{
    background-color: $secondPurple;
  }
</style>
