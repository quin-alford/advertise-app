<template>
  <div class="place">
		<Identication
			continent="Asia"
			country="Singapore"
			place="Strenous Travel Style"
			idNumber="09781021"
		/>

		<Title>
			<template #title>
				Marina Bay Sands Observation
			</template>
			<template #description>
				A great spot for PR; order yourselft a drink from the bar and get comfortable on one of the day beds that line the impressive 100-metre pool.
			</template>
		</Title>

		<PlaceList />
	</div>
</template>

<script>
import Title from "@/components/Shared/Title";
import Identication from "./Identication";
import PlaceList from "./PlaceList";

export default {
	name: "Place",
	components: {
		Title,
		Identication,
		PlaceList,
	},
};
</script>

<style scoped>
.place {
	border: 1px solid lightgray;
	border-radius: 0.25rem;
	padding: 1.5rem;
}
.place__info {
	display: flex;
	justify-content: space-between;
	margin-bottom: 2rem;
}
</style>