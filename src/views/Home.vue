<template>
  <div class="home">
    <Travel />
  </div>
</template>

<script>
import Travel from "@/components/Travel";

export default {
	name: "Home",
	components: {
		Travel,
	},
};
</script>

<style scoped>
.home {
	max-width: 1200px;
	margin-left: auto;
	margin-right: auto;
}
</style>
