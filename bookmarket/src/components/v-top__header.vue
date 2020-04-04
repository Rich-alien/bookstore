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
  queue{
		
	}
</style>
