<template>
  <div id="app">
    <WishHeader></WishHeader>
    <WishInput></WishInput>
    <WishList></WishList>
    <WishFooter></WishFooter>
  </div>
</template>

<script>
import WishHeader from './components/WishHeader.vue'
import WishInput from './components/WishInput.vue'
import WishList from './components/WishList.vue'
import WishFooter from './components/WishFooter.vue'

export default {
  components:{
    'WishHeader': WishHeader,
    'WishInput': WishInput,
    'WishList': WishList,
    'WishFooter': WishFooter
  }
}
</script>

<style lang="css">

</style>
