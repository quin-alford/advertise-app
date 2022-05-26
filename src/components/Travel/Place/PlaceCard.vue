<template>
  <div class="place-card">
    <img class="place-card__image" :src="placeImage" />
    <div class="place-card__detail">
      <div class="place-card__detail-title">
        <div class="place-card__detail-title-day">
          {{ placeDay }}
        </div>
        <div class="place-card__detail-title-name">
          {{ placeName }}
        </div>
      </div>
      <div class="place-card__detail-comment">
        {{ placeComment }}
      </div>
      <div class="place-card__detail-link">
        Show more
      </div>
    </div>
  </div>
</template>

<script>
export default {
	name: "PlaceCard",
	props: {
		place: {
			type: Object,
			default: () => {},
		},
	},
	computed: {
		placeImage() {
			return this.place.image;
		},
		placeDay() {
			return `Day ${this.place.day}`;
		},
		placeName() {
			return this.place.name;
		},
		placeComment() {
			return this.place.comment;
		},
		placeLink() {
			return this.place.link;
		},
	},
};
</script>

<style scoped>
.place-card {
	position: relative;
	margin-top: 1rem;
	display: grid;
	grid-template-columns: 1fr 2fr;
	grid-gap: 1.5rem;
}
.place-card__image {
	width: 100%;
	height: 160px;
	border-radius: 5px;
}
.place-card__detail-title {
	display: flex;
	gap: 1rem;
	margin-bottom: 1rem;
}
.place-card__detail-title-day {
	font-size: 20px;
	font-weight: bold;
	color: darkblue;
}
.place-card__detail-title-name {
	font-size: 20px;
	font-weight: bold;
	color: black;
}
.place-card__detail-comment {
	font-size: 18px;
	font-weight: 500;
	color: gray;
}
.place-card__detail-link {
	position: absolute;
	bottom: 0;
	font-size: 16px;
	font-weight: 500;
	color: darkblue;
	cursor: pointer;
}
</style>