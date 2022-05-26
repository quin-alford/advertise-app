<template>
  <div class="rate">
    <img v-for="index in 5" :key="index" :src="index < rateNumber ? '@/assets/img/red-star.png' : '@/assets/img/empty-star.png'">
  </div>
</template>

<script>
export default {
	name: "Rate",
	props: {
		rate: {
			type: Number,
			required: true,
			default: 5,
		},
	},
	computed: {
		rateNumber() {
			return this.rate;
		},
	},
};
</script>

<style scoped>
.rate {
	display: flex;
	justify-content: center;
	gap: 0.25rem;
}
</style>