<template>
  <div class="app-container">
    <!-- 头部 -->
    <mt-header fixed title="云购"></mt-header>
  <!-- 底部 -->
  <nav class="mui-bar mui-bar-tab">
			<router-link class="mui-tab-item " to="/home">
				<span class="mui-icon mui-icon-home"></span>
				<span class="mui-tab-label">首页</span>
			</router-link>
				<router-link class="mui-tab-item" to="/member">
				<span class="mui-icon mui-icon-contact"></span>
				<span class="mui-tab-label">会员</span>
			</router-link>
			<router-link class="mui-tab-item" to="/shopcar">
				<span class="mui-icon mui-icon-extra mui-icon-extra-cart">
          	<span class="mui-badge">0</span>
        </span>
				<span class="mui-tab-label">购物车</span>
			</router-link>
			<router-link class="mui-tab-item" to="/search">
				<span class="mui-icon mui-icon-gear"></span>
				<span class="mui-tab-label">搜索</span>
			</router-link>
		</nav>
  <!-- 中间内容区域 -->
			<transition>
			<router-view></router-view>
			</transition>
  </div>
</template>

<script>
export default {
  name: "App"
};
</script>

<style lang="less">
.app-container {
  padding-top: 40px;
	padding-bottom: 50px;
	overflow-x: hidden;
	.v-enter{
		transform: translateX(100%);
		opacity: 0;
	}
	.v-leave-to{
		position: absolute;
		opacity: 0;
		transform: translateX(-100%);
	}
	.v-enter-active,
	.v-leave-active{
		transition: all 0.3s ease;
	}
}
</style>

