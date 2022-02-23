<template>
<link href="http://fonts.cdnfonts.com/css/justice-league" rel="stylesheet">
  <div>
    <Header />
  </div>
  <div class="main">
    <Cards />
  </div>
  <div>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue"
import Cards from "./components/Cards.vue"
import Footer from "./components/Footer.vue"

export default {
  name: 'App',
  components: {
    Header,
    Cards,
    Footer
  }
};
</script>

<style lang="scss">
@import '@/assets/scss/main.scss';

.main {
  background-image: url(../public/img/bg-dark.png);
  height: 700px;
}
</style>
