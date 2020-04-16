<style scoped lang="scss">
	.header{
		background-color: #EDEDED;
	}
	.container{
		display: flex;
		max-width: 1001px;
		margin: auto;
		justify-content: space-between;
		align-items: center;
	}
	.logo{
		margin: 20.8px 0 14.7px 0;
	}
	form {
  position: relative;
  width: 457px;
  margin: 0 auto;
}
.search {
	background: #A3D0C3;
	height: 40;
	}
.search input {
  width: 100%;
  height: 40px;
  padding-left: 10px;
  border: 4px solid #79D260;
  border-radius: 5px;
  outline: none;
  background: #fff;
  color: rgb(49, 49, 49);
}
.search button {
  position: absolute; 
  top: 0;
  right: 0px;
  width: 124px;
  height: 40px;
  border: none;
  background: #79D260;
  border-radius: 0 5px 5px 0;
  cursor: pointer;
	color:white;
	font-size: 22px;

}
//	добавить иконку
.search button:before {
  content: "";
	background-image: url("/src/assets/header__img/search.svg");
	height: 24px;
	width: 24px;
  font-size: 16px;
  color: #F9F0DA;
}
.basketWish{
	display: flex;
	align-items: center;
}
.basket{
	display: flex;
	flex-direction: column;
	border-right: 1px solid #C3C3C3;
	padding-right: 7px;
	margin-right: 25px;
	&__top{
		display: flex;
		flex-direction: row;
		align-items: center;
		margin-bottom: 10px;
		&-icon{
			margin-right: 5px;
		}
		&-name{
			margin-right: 3px;
			color: #6D6D6D;
		}
		&-number{
			font-size: 14px;
			color: #6D6D6D;
		}
	}
	&__bottom{
		display: flex;
		flex-direction: row;
		align-items: center;
		// margin-top: 10px;
		&-price{
			font-size: 20px;
			margin-right: 30px;
			color: #6D6D6D;
			font-size: 27px;
			font-weight: 700;
		}
		&-checkout{
			background-color: black;
			color: white;
			padding: 7px 15px 7px 10px;
		}
	}

}

</style>

<template>
<div class="header">
	<div class="container">
		<img src="../assets/header__img/logo.png" alt="" class="logo">
			<div class="search">
				<form>
				<input type="text">
				<button type="submit">Search</button>
				</form>
			</div>
			<div class="basketWish">
				<div class="basket">
				<div class="basket__top">
						<img src="../assets/header__img/icon.svg" alt="" class="basket__top-icon">
						<div class="basket__top-name">Your cart</div>
						<div class="basket__top-number">( {{number}} items )</div>
					<!-- если чисел больше 1 то items !! не забудь написать логику данного момента  -->
				</div>
				<div class="basket__bottom">
					<div class="basket__bottom-price"> $ {{price}} </div>
					<!-- подсчет суммы -->
					<button class="basket__bottom-checkout">Chekout</button>
					<!-- при нажатии открывается компонент с списком книг -->
				</div>
				</div>
				<div class="wish">
					<img src="../assets/header__img/wish.svg" alt="" class="wish-icon">
					<h3 class="wish-name">Wish list</h3>
				</div>
			</div>
	</div>
</div>

</template>

<script>
export default {
  data: function() {
    return{
			number: 3,
			price: 123,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
