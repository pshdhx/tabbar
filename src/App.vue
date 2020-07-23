<template>
  <div id="app">
    <tab-bar>
      <tab-bar-item path="/home" activeColor="blue">    <!-- 为什么不加:，因为不是从相应系统中取得，用的就是字符串而不是变量 -->
        <img src="./assets/img/tabbar/home.svg" slot="item-icon" >
        <img src="./assets/img/tabbar/home_active.svg" slot="item-icon-active" >
        <div slot="item-text">首页</div>
      </tab-bar-item>
      <tab-bar-item path="/category">  
         <img src="./assets/img/tabbar/category.svg" slot="item-icon" >
          <img src="./assets/img/tabbar/home_active.svg" slot="item-icon-active" >
         <div slot="item-text">分类</div>
      </tab-bar-item>
        <tab-bar-item path="/cart">   
          <img src="./assets/img/tabbar/shopcart.svg" slot="item-icon" >
           <img src="./assets/img/tabbar/home_active.svg" slot="item-icon-active" >
          <div slot="item-text">购物车</div>
         </tab-bar-item>
         <tab-bar-item path="/profile">      
            <img src="./assets/img/tabbar/profile.svg" slot="item-icon" >
             <img src="./assets/img/tabbar/home_active.svg" slot="item-icon-active" >
              <div slot="item-text">我的</div>
         </tab-bar-item>
    </tab-bar>
    <router-view></router-view>
  </div>
</template>

<script>
import TabBar from './components/tabbar/TabBar'
import TabBarItem from './components/tabbar/TabBarItem'
export default {
  name: 'App',
  components:{
    TabBar,
    TabBarItem
  }
}
</script>

<style>
  @import "./assets/css/base.css";
  #tab-bar{
    display: flex;
    background-color: #f6f6f6;
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
    box-shadow: 0 -3px 1px rgba(100,100, 100, 0.2);
  }
  .tab-bar-item{
    flex:1;
    text-align: center;
    height: 49px;
  }
</style>
