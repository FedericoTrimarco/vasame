<template>
  <div id="app">
    <Header />

    <main>
      <SectionOne />
      <SectionTwo />
      <SectionThree />
      <SectionFour />
    </main>

    <Footer />
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import SectionOne from '@/components/SectionOne.vue'
import SectionTwo from '@/components/SectionTwo.vue'
import SectionThree from '@/components/SectionThree.vue'
import SectionFour from '@/components/SectionFour.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    SectionOne,
    SectionTwo,
    SectionThree,
    SectionFour,
    Footer,
  }
}
</script>

<style lang="scss">
@import './style/variables.scss';
@import './style/utilities.scss';
#app{
  background-color: $secondPurple;

  a{
    color: $thirdPurple;
    text-decoration: none;
    &:hover{
      text-decoration: underline;
    }
  }
}

</style>
