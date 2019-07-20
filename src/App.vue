<template>
  <div class="top">
    <!-- Header 区域 -->
    <mt-header fixed title="黑马程序员 · Vue项目"></mt-header>

    <!-- 中间的  router-view 区域 -->
    <transition>
      <router-view></router-view>
    </transition>

    <!-- 底部的 Tabber 区域 -->
    <nav class="mui-bar mui-bar-tab">
      <router-link to="/home" class="mui-tab-lib">
        <span class="mui-icon mui-icon-home"></span>
        <span class="mui-tab-label">首页</span>
      </router-link>
      <router-link to="/member" class="mui-tab-lib">
        <span class="mui-icon mui-icon-contact"></span>
        <span class="mui-tab-label">会员</span>
      </router-link>
      <router-link to="/shopcar" class="mui-tab-lib">
        <span class="mui-icon mui-icon-extra mui-icon-extra-cart">
          <span class="mui-badge">0</span>
        </span>
        <span class="mui-tab-label">购物车</span>
      </router-link>
      <router-link to="/search" class="mui-tab-lib">
        <span class="mui-icon mui-icon-search"></span>
        <span class="mui-tab-label">搜索</span>
      </router-link>
    </nav>
  </div>
</template>

<script>
</script>

<style scoped>
.top {
  padding-top: 40px;
  overflow-x: hidden;
}

.v-enter,
.v-leave-to {
  opacity: 0;
}
.v-enter {
  transform: translateX(100%);
}
.v-leave-to {
  transform: translateX(-100%);
  position: absolute;
  z-index: 999;
}

.v-enter-active,
.v-leave-active {
  transition: all 0.4s linear;
}
.mui-bar-tab .mui-tab-lib {
  display: table-cell;
  overflow: hidden;
  width: 1%;
  height: 50px;
  text-align: center;
  vertical-align: middle;
  white-space: nowrap;
  text-overflow: ellipsis;
}
.mui-active {
    color: #007aff;
}
</style>


