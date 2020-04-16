<template>
  <div class="topHeader">
    <ul class="queue">
      <li class="queue__link">{{l1}}</li>
      <li class="queue__link">{{l2}}</li>
      <li class="queue__link">{{l3}}</li>
      <li class="queue__link">{{l4}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      l1: 'Sign in',
      l2: 'My Account',
      l3: 'Order Status',
      l4: 'Help'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .topHeader{
    display: flex;
    background-color: #707070;
  }
  .queue{
    max-width: 1001px;
    margin: auto;
    width: 100%;
    display: flex;
    justify-content: flex-end;
      &__link {
        list-style-type: none;
        color: #fff;
        font-size: 20px;
        margin: 4px 0;
        padding-left: 20px;
      }
    }

      
  
    


    
	

</style>
