<template>
  <Splide  :options="{ rewind: true }">
    <SplideSlide>
      <img src="image1.jpg" alt="Sample 1">
    </SplideSlide>
    <SplideSlide>
      <img src="image2.jpg" alt="Sample 2">
    </SplideSlide>
  </Splide>
</template>

<script>
import { Splide, SplideSlide } from '@splidejs/vue-splide';
import { defineComponent } from 'vue';
import '@splidejs/splide/dist/css/themes/splide-default.min.css';

export default defineComponent( {
  components: { Splide, SplideSlide },
} );
</script>

