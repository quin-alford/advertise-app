<template>
  <div class="information">
    <Place />
    <Price />
  </div>
</template>

<script>
import Place from "./Place/index";
import Price from "./Price/index";

export default {
	name: "Information",
	components: {
		Place,
		Price,
	},
};
</script>

<style scoped>
.information {
	display: grid;
	grid-template-columns: 2fr 1fr;
	grid-gap: 1.5rem;
}
</style>