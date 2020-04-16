<template>
  <div class="home">
    <topHeader/>
    <Header/>
    <navigation/>
    <suggestion/>
    <bookCatalog/>
  </div>
</template>

<script>
import topHeader from '@/components/v-top__header.vue'
import Header from '@/components/v-header.vue'
import navigation from '@/components/v-navigation.vue'
import suggestion from '@/components/v-suggestion.vue'
import bookCatalog from '@/components/v-bookCatalog.vue'

export default {
  name: 'Home',
  components: {
    topHeader,
    Header,
    navigation,
    suggestion,
    bookCatalog
  }
}
</script>
