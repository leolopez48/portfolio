<template>
  <carousel :items-to-show="1">
    <slide v-for="image in images" :key="image">
      <img
        class="img-fluid"
        v-bind:src="require('@/assets/' + image)"
        alt=""
        loading="lazy"
      />
    </slide>

    <template #addons>
      <navigation />
      <pagination />
    </template>
  </carousel>
</template>

<script>
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";

export default {
  name: "App",
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
  props: {
    images: Array,
  },
};
</script>