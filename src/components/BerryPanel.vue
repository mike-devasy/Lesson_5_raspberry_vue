<template>
	<div class="panel-container">
<berry-card v-for="card in cardsListData" :key="card.id"  :card-data="card"/>
	</div>
</template>

<script>
import BerryCard from './BerryCard.vue'
	export default {
	name:'BerryPanel',
  components: { BerryCard },
		props: {
		cardsListData: {
				type: Array,
				default: ()=>[],
			},
		},
	}
</script>

<style lang="css" scoped>
.panel-container{
	color: ;
	height: 300px;
	display: inline-flex;
	background-color: black;
}
</style>