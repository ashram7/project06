<template lang="html">
  <div>
    <input type="text" v-model="newWishItem" />
    <button v-on:click="addWish">추가</button>
  </div>
</template>

<script>
export default {
  data(){
    return {
      newWishItem:''
    }
  },
  methods:{
    addWish(){
      if(this.newWishItem !== ""){
        var value = this.newWishItem && this.newWishItem.trim();
        //console.log(this.newWishItem);
        //localStorage.setItem(this.newWishItem, this.newWishItem);
        localStorage.setItem(value, value);
        this.clearInput()
      }
    },
    clearInput(){
      this.newWishItem = '';
    }
  }
}
</script>

<style lang="css" scoped>
</style>
