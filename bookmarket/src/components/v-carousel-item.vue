<style scoped lang="scss">
	.carouselItem{
		display: flex;
		align-items: center;
		margin-top: 42px;
	}
	.text{
		color: white;
		font-size: 47px;
		width: 335px;
	}
	.img{
		height: 181px;
		width: 121px;
	}
</style>
<template>
  <div class="carouselItem">
		<img class="img" :src=" require('../assets/images/' + item_data.img)" alt="">
		<div class="text" >{{item_data.nameBook}}</div>
  </div>
</template>

<script>
export default {
	props: {
		item_data:{
			type: Object,
			default:() =>{}
		}
	},
  data: function() {
    return{

    }
  }
}
</script>




