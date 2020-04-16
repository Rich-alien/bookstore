<style scoped lang="scss">
.book{
  display: flex;
  max-width: 1001px;
	margin: auto;
	justify-content: space-between;
  margin-top: 14px;
	// align-items: center;
  &__categories{
    border: 1px solid rgba(0,0,1,0.16);
    max-width: 188px;
    &-name{
      color: #6d6969;
      font-size: 24px;
      margin:11px 63px 7px 18px;
    }
    &-btn{
      cursor: pointer;
      font-size: 17px;
      background-image: linear-gradient(to top, #79b260 0% , #92d774 100%);
      text-align: start;
      color: #fff;
      text-transform: uppercase;
      padding: 7px 21px;
    }
    &-view{
      text-align: start;
      margin-top: 43px;
      margin-left: 25px;
      margin-bottom: 43px;
      margin-right: 25px;
      
      &-link{
        line-height: 26.67px;
        border-bottom: 1px solid #000;
        margin-bottom: 3px;
        cursor: pointer;
      }
    }

  }
  &__view{
    border: 1px solid black;
    width: 798px;
    &__item{
    display: flex;
    flex-wrap: wrap;
      &-img{
        width: 98px;
        height: 149px;
      }
    }
  }

}
.db{
  display: flex;
}
.dn{
 display: none;
  
}

</style>
<template>
  <div class="book">
		<div class="book__categories">
      <div class="book__categories-name">Categories</div>
      <div @click="isShow" class="book__categories-btn">All</div>
      <div v-if="showCatal" class="book__categories-view">
      <div @click="itFantasy" class="book__categories-view-link">Fantasy</div>
			<div @click="itMystery" class="book__categories-view-link">Mystery</div>
			<div @click="itNews" class="book__categories-view-link">News</div>
			<div @click="itHorror" class="book__categories-view-link">Horror</div>
			<div @click="itPoetry"  class="book__categories-view-link">Poetry</div>
			<div @click="itRomance" class="book__categories-view-link">Romance</div>
			<div @click="itCook" class="book__categories-view-link">Cook</div>
			<div @click="itChildren" class="book__categories-view-link">Children</div>
      </div>
    </div>
    <div class="book__view" >
      <!-- <bookviewitems> -->
        <!-- </bookviewitems> -->
        <!-- db:childrenIsActive  -->
        <children class="db" v-bind:class="{dn : childrenIsActive}"></children> 
        <cook   class="db"  v-bind:class="{dn : cookIsActive}" />
        <fantasy  class="db" v-bind:class="{dn : fantasyIsActive}" />
        <mystery class="db"  v-bind:class="{dn : mysteryIsActive}" />
        <news  class="db" v-bind:class="{dn : newsIsActive}"  />
        <horror  class="db"  v-bind:class="{dn : horrorIsActive}" />
        <poetry  class="db"   v-bind:class="{dn : poetryIsActive}" />
        <romance class="db"  v-bind:class="{dn : romanceIsActive}" />
      </div>
      
    </div>
</template>

<script>
// import posts from "../posts";
// import bookviewitems from '@/components/v-bookviewitems.vue'

import children from '@/components/categories/v-Children.vue'
import cook from '@/components/categories/v-Cook.vue'
import fantasy from '@/components/categories/v-Fantasy.vue'
import mystery from '@/components/categories/v-Mystery.vue'
import news from '@/components/categories/v-News.vue'
import horror from '@/components/categories/v-Horror.vue'
import poetry from '@/components/categories/v-Poetry.vue'
import romance from '@/components/categories/v-Romance.vue'
export default {
  name:"zero",
  components: {
  // bookviewitems,
  children,
  cook,
  fantasy,
  mystery,
  news,
  horror,
  poetry,
  romance
  },
  data: function() {
    
    return{
      showCatal: true,

      childrenIsActive:false,
      cookIsActive:true,
      fantasyIsActive:true,
      mysteryIsActive:true,
      newsIsActive:true,
      horrorIsActive:true,
      poetryIsActive:true,
      romanceIsActive:true,
    }
  },
   methods: {
     isShow : function(){
       this.showCatal = !this.showCatal;
     },



     itNews: function(){

      this.newsIsActive=false;
      this.childrenIsActive=true;
      this.cookIsActive=true;
      this.fantasyIsActive=true;
      this.mysteryIsActive=true;
      this.horrorIsActive=true;
      this.poetryIsActive=true;
      this.romanceIsActive=true;

     },
     itFantasy: function(){

      this.fantasyIsActive=false;
      this.childrenIsActive=true;
      this.cookIsActive=true;

      this.mysteryIsActive=true;
      this.horrorIsActive=true;
      this.poetryIsActive=true;
      this.romanceIsActive=true;
      this.newsIsActive=true;
     },
     itMystery: function(){

      this.mysteryIsActive=false;
      this.childrenIsActive=true;
      this.cookIsActive=true;
      this.fantasyIsActive=true;
      this.horrorIsActive=true;
      this.poetryIsActive=true;
      this.romanceIsActive=true;
       this.newsIsActive=true;

     },
     itHorror: function(){

      this.horrorIsActive=false;
      this.childrenIsActive=true;
      this.cookIsActive=true;
      this.fantasyIsActive=true;
      this.mysteryIsActive=true;

      this.poetryIsActive=true;
      this.romanceIsActive=true;
       this.newsIsActive=true;
     },
     itPoetry: function(){

      this.poetryIsActive=false;
      this.childrenIsActive=true;
      this.cookIsActive=true;
      this.fantasyIsActive=true;
      this.mysteryIsActive=true;
      this.horrorIsActive=true;

      this.romanceIsActive=true;
       this.newsIsActive=true;
     },
     itCook: function(){

      this.cookIsActive=false;
      this.childrenIsActive=true;

      this.fantasyIsActive=true;
      this.mysteryIsActive=true;
      this.horrorIsActive=true;
      this.poetryIsActive=true;
      this.romanceIsActive=true;
       this.newsIsActive=true;
     },
     itRomance: function(){

      this.romanceIsActive=false;
      this.childrenIsActive=true;
      this.cookIsActive=true;
      this.fantasyIsActive=true;
      this.mysteryIsActive=true;
      this.horrorIsActive=true;
      this.poetryIsActive=true;

       this.newsIsActive=true;
     },
     itChildren: function(){

      this.childrenIsActive=false;
      this.cookIsActive=true;
      this.fantasyIsActive=true;
      this.mysteryIsActive=true;
      this.horrorIsActive=true;
      this.poetryIsActive=true;
      this.romanceIsActive=true;
       this.newsIsActive=true;
     },
   },

  
}
</script>




