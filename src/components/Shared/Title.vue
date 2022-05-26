<template>
  <div>
    <div class="title">
      <slot name="title"></slot>
    </div>
    <div class="description">
      <slot name="description"></slot>
    </div>
  </div>
</template>

<script>
export default {
	name: "Title",
};
</script>

<style scoped>
.title {
	font-size: 36px;
	font-weight: bold;
	color: black;
}
.description {
	margin-top: 1rem;
	font-size: 20px;
	font-weight: 500;
	color: black;
}
</style>