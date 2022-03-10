<template>
  <Splide :options="{ rewind: true }">
    <SplideSlide v-for="heroe in heroes" :key="heroe.id">
      <Card :data="heroe" :isDarkMode="isDarkMode" />
    </SplideSlide>
  </Splide>
</template>

<script>
import Card from "./Card.vue";
import { heroes } from "@/data/db.json";
import { Splide, SplideSlide } from "@splidejs/vue-splide";
import "@splidejs/splide/dist/css/themes/splide-default.min.css";

export default {
  name: "Carrossel",
  components: { Splide, SplideSlide, Card },
  data() {
    return {
      heroes,
    };
  },
  props: {
    isDarkMode: { type: Boolean, required: true },
  },
};
</script>

<style lang="scss" scoped>

</style>

