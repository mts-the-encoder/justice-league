<template>
  <link href="http://fonts.cdnfonts.com/css/justice-league" rel="stylesheet" />
  <div>
    <Header />
  </div>
  <div class="main" :class="{ 'bg-dark': isDarkMode }">
    <label>
      <span class="text">modo escuro</span>
      <input type="checkbox" class="dark" @click="isDarkMode = !isDarkMode" />
      <span class="check"></span>
    </label>
    <Carroussel :isDarkMode="isDarkMode"/>
  </div>
  <div>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Carroussel from "./components/Carroussel.vue"

export default {
  name: "App",
  components: {
    Header,
    Footer,
    Carroussel
  },
  data() {
    return {
      isDarkMode: true,
    };
  },
};
</script>

<style lang="scss">
@import "@/assets/scss/main.scss";
@import "@/assets/scss/_fonts.scss";
@import "@/assets/scss/_variables.scss";
@import "@/assets/scss/_reset.scss";

.main {
  background-image: url(assets/img/bg-light.png);
  height: 600px;
  &.bg-dark {
    background-image: url(assets/img/bg-dark.png);
  }
  label {
    margin: 0;
    display: flex;
    justify-content: flex-end;
    align-items: flex-end;
    margin-right: 50px;
  }
  .dark {
    -webkit-appearance: none;
    visibility: hidden;
    display: none;
  }
  .check {
    position: relative;
    background: $red;
    cursor: pointer;
    border-radius: 20px;
    overflow: hidden;
    transition: ease-in 0.5s;
    margin-top: 15px;
    height: 20px;
    width: 40px;
  }
  .dark:checked ~ .check {
    background: #000;
  }
  .check::before {
    content: '';
    position: absolute;
    top: 2px;
    left: 2px;
    background-color: $greyLight;
    width: 16px;
    height: 16px;
    border-radius: 10%;
    transition: 0.5s;
    transform: translate(-50px);
  }
  .dark:checked ~ check::before {
    transform: translate(-50px);
  }
  .check::after {
    content: '';
    position: absolute;
    top: 2px;
    left: 20px;
    background: $greyLight;
    width: 16px;
    height: 16px;
    border-radius: 50%;
    transition: 0.5s;
    transform: translate(50px);
  }
  .dark:checked ~ check::after {
    transform: translate(50px);
  }
  .text{
    font-size: 17px;
    margin-top: 5px;
    font-family: 'JUSTICE LEAGUE', sans-serif;
    color: $greyDark
 }
}
</style>
