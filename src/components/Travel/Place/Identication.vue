<template>
  <div class="identication">
    <div class="identication__country">
      {{ location }}
    </div>
    <div class="identication__id">
      {{ id }}
    </div>
  </div>
</template>

<script>
export default {
	name: "Identication",
	props: {
		continent: {
			type: String,
			required: true,
			default: "",
		},
		country: {
			type: String,
			required: true,
			default: "",
		},
		place: {
			type: String,
			required: true,
			default: "",
		},
		idNumber: {
			type: String,
			required: true,
			default: "",
		},
	},
	computed: {
		location() {
			return `${this.continent}  >  ${this.country}  >  ${this.place}`;
		},
		id() {
			return `ID: ${this.idNumber}`;
		},
	},
};
</script>

<style scoped>
.identication {
	width: 100%;
	display: flex;
	justify-content: space-between;
	margin-bottom: 2rem;
}
.identication__country {
	font-size: 16px;
	font-weight: 700;
	color: gray;
}
.identication__id {
	font-size: 16px;
	font-weight: 700;
	color: gray;
}
</style>