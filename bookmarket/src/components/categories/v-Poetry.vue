
<style scoped lang="scss">
.book{
	display: flex;
	flex-wrap:wrap;
	
	&__view{
		// border: 3px solid black;
		margin:15px 30px ;
		&-img{
			width: 98px;
			height: 149px;
			margin-bottom: 17px;
		}
		&-name{
			max-width: 110px;
			color: #595959;
			font-size: 15px;
			height: 65px;
		}
		&-price{
			color:#f05356;
			font-size: 22px;
		}
	}
}
</style>
<template>
  <div class="book">
		<div v-for="post in posts" :key="post.id"  class="book__view" v-show="post.style == cat" >
        <img  class="book__view-img" :src=" require('./assets/bookimg/' + post.image)" alt="">
        <div  class="book__view-name"> {{ post.name}}</div>
					<div class="book__view-price">${{post.price}}</div>
  	</div>
	</div>
</template>

<script>
import posts from "./posts";
export default {
  name:"posi",
  data: function() {
    
    return{
      showCatal: true,
      posts: posts,
      cat: 'Poetry',
    }
  },
   
  
}
</script>




