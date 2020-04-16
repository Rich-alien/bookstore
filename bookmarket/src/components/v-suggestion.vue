<style scoped lang="scss">
	.suggestion{
		display: flex;
		max-width: 1001px;
		margin: auto;
		justify-content: space-between;
		align-items: center;
		&__slider{
			width: 714px;
			height: 304px;
			border: 1px solid black;
			margin-top: 13px;
			background: -webkit-linear-gradient(63deg, #151515 5px, transparent 5px) 0 5px,
            -webkit-linear-gradient(243deg, #151515 5px, transparent 5px) 10px 0px,
            -webkit-linear-gradient(63deg, #222 5px, transparent 5px) 0px 10px,
            -webkit-linear-gradient(243deg, #222 5px, transparent 5px) 10px 5px,
            -webkit-linear-gradient(0deg, #1b1b1b 10px, transparent 10px),
            -webkit-linear-gradient(#1d1d1d 25%, #1a1a1a 25%, #1a1a1a 50%, transparent 50%, transparent 75%, #242424 75%, #242424);
			background: -moz-linear-gradient(63deg, #151515 5px, transparent 5px) 0 5px,
									-moz-linear-gradient(243deg, #151515 5px, transparent 5px) 10px 0px,
									-moz-linear-gradient(63deg, #222 5px, transparent 5px) 0px 10px,
									-moz-linear-gradient(243deg, #222 5px, transparent 5px) 10px 5px,
									-moz-linear-gradient(0deg, #1b1b1b 10px, transparent 10px),
									-moz-linear-gradient(#1d1d1d 25%, #1a1a1a 25%, #1a1a1a 50%, transparent 50%, transparent 75%, #242424 75%, #242424);
			background: linear-gradient(27deg, #151515 5px, transparent 5px) 0 5px,
									linear-gradient(207deg, #151515 5px, transparent 5px) 10px 0px,
									linear-gradient(27deg, #222 5px, transparent 5px) 0px 10px,
									linear-gradient(207deg, #222 5px, transparent 5px) 10px 5px,
									linear-gradient(90deg, #1b1b1b 10px, transparent 10px),
									linear-gradient(#1d1d1d 25%, #1a1a1a 25%, #1a1a1a 50%, transparent 50%, transparent 75%, #242424 75%, #242424);
			background-size: 20px 20px;
			background-color: #131313;	
		}
	}
	.suggestion__discount{
		display: flex;
		flex-direction: column;
		align-items: center;
		background-color: #6d6d6d;
		margin-top: 13px;
	}
	.sd{
		&-name{
			color: #fff;
			font-size: 27px;
			margin: 9px 24px 0px;
		}
		&-nameBook{
			font-size: 15px;
			color: #fff;
			font-weight: 300px;
			margin-top: 8px;
		}
		&-img{
			width: 84px;
			height: 111px;
			margin-top: 11px;
		}
		&-underBook{
			width: 175px;
			height: 12px;
			fill: white;
		}
		&-saveNumber{
			margin-top: 25px;
			font-size: 11px;
			color: #fff;
			font-weight: 300;
		}
		&-Price{
			font-size: 29px;
			color: #fff;
			margin-top: 4px;
		}
		&-btn{
			text-shadow: 1px 1px 1px rgba(74, 151, 74, 0.75);
			border: 1px solid #52a452;
			background-image: linear-gradient(to top, #52a452 0%, #61c261 100%);
			padding: 7px 15px 3px 19px;
			margin: 7px 0 7px;

		}
	}

</style>
<template>
  <div class="suggestion">
		<div class="suggestion__slider">
			<vCarousel
			
			:carousel_data="sliderItems"
			/>
		</div>
		<div class="suggestion__discount">
			<div class="sd-name">
				{{sdName}}
			</div>
			<div class="sd-nameBook">
				{{sdNameBook}}
			</div>
			<img class="sd-img" :src=" require('../assets/images/' + imgBook)" alt="">
			<!-- <svg class="sd-underBook">
			<polygon points="0 0,2 3" style="fill: white;"/>
			</svg> -->
			<div class="sd-saveNumber">
					{{saveNumber}}
			</div>
			<div class="sd-Price">
				{{Price}}
				
			</div>
			<button class="sd-btn">{{btnName}}</button>
		</div>
  </div>
</template>

<script>
import vCarousel from './v-carousel'
export default {
	components: {
		vCarousel,
	},
  data: function() {
    return{
			sliderItems: [
				{id: 1, name: 'img1', nameBook: 'Marathon Baba', img: '1.png'},
				{id: 2, name: 'img2', nameBook: 'Tne Hare With Amber Eyes', img: '2.png'},
				{id: 3, name: 'img3', nameBook: 'Can Love Happy Juse?', img: '3.png'},
				{id: 4, name: 'img4', nameBook: 'John Grisham', img: '4.png'},
				{id: 5, name: 'img5', nameBook: 'Tne war god', img: '5.png'}
			],
			sdName:'Deal of the Month',
			sdNameBook: 'The Human Fase of Big Data',
			imgBook:'5.png',
			saveNumber: 'Save 45% Today',
			Price: '$27.50',
			btnName: 'Buy now'
    }
  }
}
</script>




