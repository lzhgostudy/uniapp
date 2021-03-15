<template lang="pug">
	.wrap
		u-form(:model="model" ref="uForm")
			u-form-item(label="结算方式")
				u-radio-group(v-model="radio" @change="radioGroupChange")
					u-radio(v-for="(item, index) in radioList" :key="index" :name="item.value") {{ item.name }}
</template>

<script>
	export default{
		data() {
			return {
				radio: 'alipay',
				radioList: [
					{
						name: '支付宝',
						value: 'alipay',
						checked: true,
						disabled: false
					},
					{
						name: '微信',
						value: 'wechat',
						checked: false,
						disabled: false
					},
					{
						name: '银联',
						value: 'union',
						checked: false,
						disabled: false
					},
					{
						name: '现金',
						value: 'cash',
						checked: false,
						disabled: false
					}
				],
				model: {
					
				}
			}
		},
		methods: {
			radioGroupChange(e) {
				console.log('radioGroupChange:', e)
			}
		}
	}
</script>

<style>
</style>
