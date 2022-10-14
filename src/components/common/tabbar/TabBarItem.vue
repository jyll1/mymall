<template>
  <div class="tab-bar-item" @click="itemClick">
    <div v-if="!isActive"><slot name="item-icon"></slot></div>
    <div v-else><slot name="item-icon-active"></slot></div>
    <div :style="activeStyle"><slot name="item-text"></slot></div>
  </div>
</template>

<script>
export default {
  name: "TabBarItem",
  props: {
    path: String,
    activeColor:{
      type:String,
      default:'red'
    }
  },
  computed: {
    isActive() {
      // $route哪个路径活跃就是哪个,下面的意思是点到哪个路径哪个路径的isActive就是true
      return this.$route.path.indexOf(this.path) !== -1
    },
    activeStyle(){
      return this.isActive ? {color: this.activeColor} : {}
    }
  },
  methods: {
    itemClick() {
      this.$router.replace(this.path).catch(err => {})
    },
  },
};
</script>

<style scoped>
.tab-bar-item {
  /* 平摊分配宽度 */
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 14px;
}
.tab-bar-item img {
  width: 24px;
  height: 24px;
  margin-top: 3px;
  /* 去掉图片底下默认的3像素 */
  vertical-align: middle;
  margin-bottom: 2px;
}
/* .active {
  color:#1296db;
} */
</style>