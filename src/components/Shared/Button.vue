<template>
  <button
    type="button"
    class="button"
    :class="{
      'btn__primary' : color === 'primary',
      'btn__secondary' : color === 'secondary',
      'btn__outline' : color === 'outline',
      'btn__active' : isActive,
      'btn__disabled' : isDisabled
    }"
    @click="click"
  >
    <slot></slot>
  </button>
</template>

<script>
export default {
	name: "Button",
	props: {
		color: {
			type: String,
			required: false,
			default: "primary",
		},
		isActive: {
			type: Boolean,
			required: false,
			default: true,
		},
		isDisabled: {
			type: Boolean,
			required: false,
			default: false,
		},
	},
	methods: {
		click() {
			this.$emit("click");
		},
	},
};
</script>

<style scoped>
.button {
	padding: 0.75rem 1rem;
	border: 1px solid grey;
	border-radius: 0.25rem;
	font-size: 16px;
	font-weight: 500;
	color: white;
	cursor: pointer;
}
.btn__primary {
	background: brown;
}
.btn__secondary {
	background: darkblue;
}
.btn__outline {
	background: transparent;
	color: white;
}
</style>