<template lang="html">
  <section>
    <ul>
      <li v-for="(wishItem, index) in propsdata" :key="wishItem" class="shadow">
        <i class="checkBtn fas fa-check" aria-hidden="true"></i>
        {{ wishItem }}
        <!--클릭 이벤트 추가-->
        <span class="removeBtn" type="button" @click="removeWish(wishItem, index)">
          <i class="far fa-trash-alt" aria-hidden="true"></i>
        </span>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  props: ['propsdata'],
  methods: {
    removeWish(wishItem, index) {
      //console.log(wishItem, index);
      //localStorage.removeItem(wishItem);
      //this.wishItems.splice(index, 1);
      this.$emit('removeWish', wishItem, index);
    }
  }
}
</script>

<style lang="css" scoped>
ul{
    list-style-type: none;
    padding-left: 0px;
    margin-top: 0px;
    text-align: left;}
li{
    display: flex; /*비율 기준의 레이아웃 방식인 flex로 지정*/
    min-height: 50px;
    height: 50px;
    line-height: 50px;
    margin: 0.5em 0;
    padding: 0 0.9em;
    background: #fefefe;
    border-radius: 5px;
    overflow: hidden;
    text-overflow: ellipsis;}
.checkBtn{
    line-height: 50px;
    color: #ff8000;
    margin-right: 5px;}
.removeBtn{
    margin-left: auto;
    color: #de4343;}
</style>
