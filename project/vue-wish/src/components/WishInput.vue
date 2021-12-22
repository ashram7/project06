<template lang="html">
  <div>
    <input type="text" v-model="newWishItem" />
    <button>추가</button>
  </div>
</template>

<script>
export default {
  data(){
    return {
      newWishItem:''
    }
  }
}
</script>

<style lang="css" scoped>
</style>
