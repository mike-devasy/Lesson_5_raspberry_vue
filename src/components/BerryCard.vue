<template>
	<a class="card-container">
<div class="card-container__image">
	<img :src="cardData.imgSrc" alt="berry">
</div>
<div class="card-container__header header-container">
	<div  class="header-container__logo">
	<img :src="cardData.logo" alt="logo"></div>
	<h3 class="header-container__title">{{cardData.companyTitle}}</h3>
	<p v-if="cardData.productInStock" class="header-container__in-stock">В наличии</p>
</div>
<p class="card-container__description">{{cardData.description}}</p>
	</a>
</template>

<script>
	export default {
		name:'BerryCard',
		props: {
			cardData: {
				type: Object,
				default:()=>({}) 
			},

		},
	}
</script>

<style lang="css" scoped>
.card-container {
	display:inline-block;
 padding: 20px 20px 0px ;
}
.card-container__image img{
border-radius: 10px;
width: 200px;
height: 200px;
}
.header-container {
 display: flex;
 align-items: center;
 gap:5px; 
 height: 20px;
}
 
.header-container__logo img{
	/* position: relative;
	z-index: 2; */
	display: inline-block;
	/* content:'' */
	width: 15px;
	height: 15px;
}
.header-container__title {
	color:rgb(225, 229, 233);
	font-size: 12px;
}

.header-container__in-stock {
	font-size: 16px;
	color:rgb(36, 213, 36);
}

.card-container__description {
	color:rgb(225, 229, 233);
	font-size: 16px;
	height: 20px;
	margin: 0;
	text-align: left;
}


</style>