<template>
  <div id="app">
    <v-header></v-header>
    <div class="tabs">
      <div class="item-tab"><router-link to="/goods">商品</router-link></div>
      <div class="item-tab"><router-link to="/ratings">评价</router-link></div>
      <div class="item-tab"><router-link to="/sellers">商家</router-link></div>
    </div>
    <router-view class="content"></router-view>
  </div>
</template>

<script>
import header from '@/components/header/header';

export default {
  components: {
    'v-header': header
  },
  name: 'app'
};

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.header{
  height:50px;
}
.tabs{
  width:100%;
  display:flex;
}
.tabs .item-tab{
  flex:1;
}
.tabs .item-tab a{
  text-decoration:none;
  display:block;
  height:40px;
  line-height:40px;
}
.content{
  margin-top:30px;
}
</style>
