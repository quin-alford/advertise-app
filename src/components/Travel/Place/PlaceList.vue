<template>
  <div class="place-list">
		<div class="place-list__title">
			Itienary
		</div>
    
		<PlaceCard v-for="(place, index) in places" :key="index" :place="place" />
  </div>
</template>

<script>
import PlaceCard from "./PlaceCard";

export default {
	name: "PlaceList",
	components: { PlaceCard },
	data() {
		return {
			places: [
				{
					day: 1,
					name: "See the largest indoor water fall in the world",
					comment:
						"Just how much mind-boggling can be packed into a 14-day holiday? Well we'll tell you. Our hot adventure pack serious punch on a journey city Singapore and Malysia.",
					image: "http://placekitten.com/200/300",
					link: "/",
				},
				{
					day: 2,
					name: "Two giant conservatories",
					comment:
						"Just how much mind-boggling can be packed into a 14-day holiday? Well we'll tell you. Our hot adventure pack serious punch on a journey city Singapore and Malysia.",
					image: "http://placekitten.com/200/300",
					link: "/",
				},
				{
					day: 3,
					name: "Singapore 21st-century botanical garden",
					comment:
						"Just how much mind-boggling can be packed into a 14-day holiday? Well we'll tell you. Our hot adventure pack serious punch on a journey city Singapore and Malysia.",
					image: "http://placekitten.com/200/300",
					link: "/",
				},
				{
					day: 4,
					name: "Super Park",
					comment:
						"Just how much mind-boggling can be packed into a 14-day holiday? Well we'll tell you. Our hot adventure pack serious punch on a journey city Singapore and Malysia.",
					image: "http://placekitten.com/200/300",
					link: "/",
				},
			],
		};
	},
};
</script>

<style scoped>
.place-list {
	margin-top: 2rem;
}
.place-list__title {
	font-size: 24px;
	font-weight: bold;
	color: darkblue;
}
</style>