<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <MainHeader />
    <DcJumbo />

    <main>
      <ProductsSection />
      <UtilityLinks />
    </main>

    <footer>
      <FooterTop />
      <FooterBot />
    </footer>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import MainHeader from './components/MainHeader.vue';
import DcJumbo from './components/DcJumbo.vue';
import ProductsSection from './components/ProductsSection.vue';
import UtilityLinks from './components/UtilityLinks.vue';
import FooterTop from './components/FooterTop.vue';
import FooterBot from './components/FooterBot.vue';

export default {
  name: 'App',
  components: {
    // HelloWorld
    MainHeader,
    DcJumbo,
    ProductsSection,
    UtilityLinks,
    FooterTop,
    FooterBot
  }
}
</script>

<style lang="scss">
 
@import './styles/commons'

</style>
