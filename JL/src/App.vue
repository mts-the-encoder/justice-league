<template>
<link href="http://fonts.cdnfonts.com/css/justice-league" rel="stylesheet">
  <div>
    <Header />
  </div>
</template>

<script>
import Header from "./components/Header.vue"

export default {
  name: 'App',
  components: {
    Header
  }
};
</script>

<style lang="scss">
@import '@/assets/scss/main.scss';
</style>
