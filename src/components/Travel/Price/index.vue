<template>
  <div class="price">
    <TripCard />
		<TravelCard />
		<MapCard />
		<ConfidenceCard />
  </div>
</template>

<script>
import TripCard from "./TripCard.vue";
import TravelCard from "./TravelCard.vue";
import MapCard from "./MapCard.vue";
import ConfidenceCard from "./ConfidenceCard.vue";
export default {
	name: "Price",
	components: { TripCard, TravelCard, MapCard, ConfidenceCard },
};
</script>