<template>
  <div>
     <!-- 该MainTabBar中不需要考虑tab-bar和tab-bar-item的样式布局，只需要按照自己的要求在tab-bar需要插入多少个tab-bar-item-->
     <tab-bar>
      <tab-bar-item path="/home" activeColor="#1296db">
        <img slot="item-icon" src="@/assets/img/tabbar/home.png" alt="" />
        <img slot="item-icon-active" src="@/assets/img/tabbar/home-active.png" alt="" />
        <div slot="item-text">首页</div>
      </tab-bar-item>
      <tab-bar-item path="/category" activeColor="#1296db">
        <img slot="item-icon" src="@/assets/img/tabbar/category.png" alt="" />
        <img slot="item-icon-active" src="@/assets/img/tabbar/category-active.png" alt="" />
        <div slot="item-text">分类</div>
      </tab-bar-item>
      <tab-bar-item path="/cart" activeColor="#1296db">
        <img slot="item-icon" src="@/assets/img/tabbar/cart.png" alt="" />
        <img slot="item-icon-active" src="@/assets/img/tabbar/cart-active.png" alt="" />
        <div slot="item-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item path="/profile" activeColor="#1296db">
        <img slot="item-icon" src="@/assets/img/tabbar/profile.png" alt="" />
        <img slot="item-icon-active" src="@/assets/img/tabbar/profile-active.png" alt="" />
        <div slot="item-text">我的</div>
      </tab-bar-item>
    </tab-bar>
  </div>
</template>

<script>
import TabBar from "../../common/tabbar/TabBar";
import TabBarItem from "../../common/tabbar/TabBarItem";

export default {
    name:'MainTabBar',
    components: { TabBar,TabBarItem },

}
</script>
