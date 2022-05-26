<template>
  <div class="travel">
    <ImageCarousel :images="images" />
    <Information />
  </div>
</template>

<script>
import ImageCarousel from "@/components/Shared/ImageCarousel";
import Information from "./Information";

export default {
	name: "Travel",
	components: {
		ImageCarousel,
		Information,
	},
	computed: {
		images() {
			return [
				{ url: "http://placekitten.com/800/300", alt: "Place 1" },
				{ url: "http://placekitten.com/800/300", alt: "Place 2" },
				{ url: "http://placekitten.com/800/300", alt: "Place 3" },
			];
		},
	},
};
</script>