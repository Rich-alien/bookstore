<style scoped lang="scss">
.wrapper{
	max-width: 450px;
	overflow: hidden;
	margin: 0 auto;
}
.carousel{
	display: flex;
	transition: all ease .5s;
}
.arrowLeft{
	height: 38px;
	width: 38px;
	position: absolute;
	transform: translateX(-335px) translateY(-107px);
	cursor: pointer;
}
.arrowRight{
	height: 38px;
	width: 38px;
	position: absolute;
	transform: translateX(296px) translateY(-107px) rotate(180deg);
	cursor: pointer;
}
</style>
<template>
	<div class="wrapper">
			<div class="carousel" :style="{ 'margin-left': '-' + (100 * currentSlideIndex) + '%'}">
			<vCarouselItem
				v-for="item in carousel_data"
				:key="item.id"
				:item_data="item"
				
			/>

	</div>
				<!-- <button @click="prevSlide">Prev</button>
				<button @click="nextSlide">Next</button> -->
				<img @click="prevSlide" class="arrowLeft" src="../assets/arrow.svg" alt="">
				<img @click="nextSlide" class="arrowRight" src="../assets/arrow.svg" alt="">
</div>
</template>

<script>

 import vCarouselItem from './v-carousel-item'

export default {
	components: {
		vCarouselItem
	},

		props: {
			carousel_data: {
				type: Array,
				default: () => []
			}
		},
  data: function() {
	
    return{
			currentSlideIndex: 0,

    }
	},
		methods: {
		prevSlide : function(){
			if(this.currentSlideIndex > 0){
				this.currentSlideIndex--
			}
			// else{
			// 	this.currentSlideIndex = 4
			// }
			
		},
		nextSlide : function(){
			if (this.currentSlideIndex < 4) {
			this.currentSlideIndex++
			}
			// else{
			// 	this.currentSlideIndex = 0
			// }
		}
	},
}
</script>




