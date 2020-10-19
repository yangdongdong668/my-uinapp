<template>
	<view class="contact">
		<image class="img" src="http://www.itcast.cn/2018czydz/images/gywmban.jpg" mode=""></image>
		<view class="info">
			<view @click="phone">
				联系电话：400-618-9090 ( 点击拨打 )
			</view>
		</view>
		<map class="map" :latitude="latitude" :longitude="longitude" :scale="scale" :markers="markers"></map>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				longitude: 120.363172,
				latitude: 30.312212,
				scale: 13,
				markers: [{
					longitude: 120.363172,
					latitude: 30.312212,
					iconPath: '../../static/icon/home-active.png',
					width: 30,
					height: 30
				}]
			}
		},
		methods: {
			phone() {
				uni.makePhoneCall({
					phoneNumber: '400-618-9090'
				})
			}
		}
	}
</script>

<style lang="scss">
	.img {
		width: 750rpx;
		height: 320rpx;
	}
	.info{
		padding:10rpx 20rpx;
		font-size:30rpx;
		view{
			line-height:80rpx;
			border-bottom:1px solid #eee;
		}
	}
	.map {
		width: 750rpx;
		height: 750rpx;
	}
</style>
