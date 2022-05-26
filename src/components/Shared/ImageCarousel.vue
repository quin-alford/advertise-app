<template>
  <Carousel
    class="carousel"
    :perPage="perPage"
    :autoplay="true"
    :autoplayTimeout="2000"
    :navigationEnabled="false"
    :paginationEnabled="false"
  >
    <slide v-for="(image, index) in images" :key="index">
      <img width="100%" :src="image.url" :alt="image.alt" />
    </slide>
  </Carousel>
</template>

<script>
import { Carousel, Slide } from "vue-carousel";

export default {
	name: "ImageCarousel",
	components: {
		Carousel,
		Slide,
	},
	props: {
		images: {
			type: Array,
			default: () => [],
		},
	},
	data() {
		return {
			perPage: 1,
		};
	},
};
</script>

<style scoped>
.carousel {
	margin-top: 1rem;
	margin-bottom: 1rem;
}
</style>