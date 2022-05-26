<template>
  <div class="card">
		<div class="card__label">
			FROM
		</div>
		<div class="card__price">
			{{ priceInfo }}
		</div>
		<div class="card__label">
			{{ personPriceInfo }}
		</div>
		<Rate :rate="rateNumber" />
		<div class="card__button">
			<Button color="primary">
				Book Trip
			</Button>
			<Button color="outline">
				Rate
			</Button>
			<Button color="outline">
				Share
			</Button>
		</div>
	</div>
</template>

<script>
import Rate from "@/components/Shared/Rate";
import Button from "@/components/Shared/Button";
export default {
	name: "TripCard",
	components: { Rate, Button },
	props: {
		price: {
			type: Number,
			default: 1300,
		},
		personPrice: {
			type: Number,
			default: 1699,
		},
		rate: {
			type: Number,
			default: 5,
		},
	},
	computed: {
		priceInfo() {
			return `${this.price} USD`;
		},
		personPriceInfo() {
			return `${this.personPrice} USD PER PERSON`;
		},
		rateNumber() {
			return this.rate;
		},
	},
};
</script>

<style scoped>
.card {
	text-align: center;
	border: 1px solid lightgray;
	border-radius: 0.25rem;
	padding: 1rem;
	margin-bottom: 1.5rem;
	background: darkslateblue;
}
.card__label {
	font-size: 20px;
	font-weight: 500;
	color: white;
	margin-bottom: 0.5rem;
}
.card__price {
	font-size: 24px;
	font-weight: 700;
	color: white;
	margin-bottom: 0.5rem;
}
.card__button {
	margin-top: 1rem;
	display: flex;
	justify-content: center;
	gap: 0.5rem;
}
</style>