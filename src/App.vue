<template>
<div class="container">
  <Header 
    heading="The creative crew" 
    subheading="Who we are"
    content="We are team of creatively diverse.  driven.  innovative individuals working in various locations from the world."
  />
  <Cards v-bind:cards="cards"/>
  <Footer/>
</div>
</template>

<script>
import Cards from './components/Cards.vue'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Cards,
    Footer
  },
  data() {
    return{
      cards: [
        {
          name: 'Bill Mahoney',
          job: 'Product Owner',
          profile: '../assets/photo1.png'
        },
        {
          name: 'Saba Cabrera',
          job: 'Art Director',
          profile: '../assets/photo2.png'
        },
        {
          name: 'Shae Le',
          job: 'Tech Lead',
          profile: '../assets/photo3.png'
        },
        {
          name: 'Skylah Lu',
          job: 'UX Designer',
          profile: '../assets/photo4.png'
        },
        {
          name: 'Griff Richards',
          job: 'Developer',
          profile: '../assets/photo5.png'
        },
        {
          name: 'Stan John',
          job: 'Developer',
          profile: '../assets/photo6.png'
        },
      ]
    }
  }
}
</script>

<style lang="scss">
@import "./scss/globals";
@import "./scss/mixins";
.container{
  min-height: 100vh;
  margin-left: auto;
  margin-right: auto;

  @include breakpoint('m'){
    max-width: 1024px;
  }
}
</style>
