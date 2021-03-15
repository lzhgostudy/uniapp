<template lang="pug">
	.container 
		uni-list
		<!-- 基本用法 -->
			uni-list-item(title="列表文字")
			uni-list-item(title="列表禁用状态" :disabled="true")
		<!-- 多行内容显示 -->	
			uni-list-item(title="列表文字" note="列表描述信息")
			uni-list-item(:disabled="true" title="列表文字" note="列表禁用状态")
		<!-- 右侧显式角标, switch -->
			uni-list-item(title="列表右侧显示角标" :show-badge="true" badge-text="12")
			uni-list-item(title="列表右侧显示switch" :show-switch="true" @switchChange="switchChange")
		<!-- 左侧显示缩略图,图标 -->
			uni-list-item(title="列表左侧带缩略图" note="列表描述信息" :thumb="thumb" thumb-size="lg" rightText="右侧文字")
			<!-- uni-list-item(title="列表左侧带扩展图标" :show-extra-icon="true" extra-icon="contact") -->
		<!-- 开启点击反馈和右侧箭头 -->
			uni-list-item(title="开启点击反馈" clickable @click="onClick")
			uni-list-item(title="默认 navigateTo 方式跳转页面" link to="/pages/index/index" @click="onClick($event, 2)")
</template>

<script>
export default {
	data() {
		return {
			thumb: 'https://vkceyugu.cdn.bspapp.com/VKCEYUGU-dc-site/460d46d0-4fcc-11eb-8ff1-d5dcf8779628.png'
		}
	},
	methods: {
		switchChange(e) {
			console.log('switch value:', e.value)
		},
		onClick(e) {
			console.log('开启点击反馈:', e)
		}
	}
} 
</script>

<style>
</style>
