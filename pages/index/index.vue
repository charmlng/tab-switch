<template>
	<view class="content">
		<aloys-tab :tabs="tabs" @change="onTabChange">
		  <view slot="content0" class="xxx">A</view>
		  <view slot="content1" class="xxx">B</view>
      <view slot="content2" class="xxx">C</view>
		</aloys-tab>
	</view>
</template>

<script>
  import aloysTab from "@/components/aloys-tab/aloys-tab.vue"
  
	export default {
		components: { aloysTab },
		data() {
      return {
				tabs: [{
				  title: 'tabA'
				},{
				  title: 'tabB'
				},{
				  title: 'tabC'
				}]
			}
		},
		onLoad() {

		},
		methods: {
      onTabChange(index) {
        uni.showToast({
          title: '切换至tab：' + index
        })
      }
		}
	}
</script>

<style>
.content{
  position: absolute;
  height: 100%;
}
.xxx{
  font-size: 42rpx;
  font-weight: bold;
  padding: 100rpx 0;
  text-align: center;
}
</style>
