<template>
  <div class="navigation">
    <nav class="nav">
      <a href="#" class="nav-link">Fantasy</a>
			<a href="#" class="nav-link">Mystery</a>
			<a href="#" class="nav-link">News</a>
			<a href="#" class="nav-link">Horror</a>
			<a href="#" class="nav-link">Poetry</a>
			<a href="#" class="nav-link">Romance</a>
			<a href="#" class="nav-link">Cook</a>
			<a href="#" class="nav-link">Children</a>
    </nav>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .navigation{
    display: flex;
    background-color: #fff;
		border-bottom: 1px solid #E6E6E6;
		border-top: 1px solid #E6E6E6;
  }
  .nav{
    max-width: 1001px;
    margin: auto;
    width: 100%;
    display: flex;
    justify-content: space-between;

      &-link {
        color: #707070;
        font-size: 19px;
        padding-left: 20px;
				text-decoration: none;
				padding: 10px;
      }
			&-link:hover{
				background-color: #80BD66;
				transition: all 0.6s;
				color: #fff;

			}
    }

      
  
    


    
	

</style>
