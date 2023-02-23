<template>
	<view class="uni-margin-wrap">
					<swiper class="swiper" circular :indicator-dots="swiperOption.indicatorDots" :autoplay="swiperOption.autoplay" :interval="swiperOption.interval"
						:duration="swiperOption.duration">
						<swiper-item>
							<!-- <view class="swiper-item uni-bg-red">A</view> -->
							<image src="../../static/wallhaven-8o2dpj_2880x1800.png" mode="aspectFill"></image>
						</swiper-item>
						<swiper-item>
							<!-- <view class="swiper-item uni-bg-green">B</view> -->
							<image src="../../static/wallhaven-7p3we9.png" mode="aspectFill"></image>
						</swiper-item>
						<swiper-item>
							<!-- <view class="swiper-item uni-bg-blue">C</view> -->
							<image src="../../static/wallhaven-6oxgp6.jpg" mode="aspectFill"></image>
						</swiper-item>
					</swiper>
	</view>
	<view class="fish-grip">
		<uni-grid :column="4" :showBorder="false">
			<uni-grid-item>
				<view class="grip-box">我</view>
			</uni-grid-item>
			<uni-grid-item>
				<view class="grip-box">爱</view>
			</uni-grid-item>
			<uni-grid-item>
				<view class="grip-box">你</view>
			</uni-grid-item>
			<uni-grid-item>
				<view class="grip-box">呀</view>
			</uni-grid-item>
		</uni-grid>

	</view>
	<uni-section title="为你推荐" type="line" padding>
		<view class="fish-card">
			<view class="fish-card-left">
				
			</view>
			<view class="fish-card-right">
				<view class="top">
					<text class="tittle">强哥当铺</text>
					<text class="integral">5.0分</text>
				</view>
				<view class="mid">
					<view>
						<text>最低消费20￥</text>
					</view>
					<view>
						<text>月售600</text>
						<text>人均20￥</text>
					</view>
				</view>
				<view class="bottom">
					<uni-tag text="内有躺椅" type="warning" :inverted="true"></uni-tag>
				</view>
			</view>
		</view>
	</uni-section>
</template>

<script setup>
import { reactive } from "vue";
	const swiperOption = reactive({
		indicatorDots:false,
		autoplay:true,
		interval: 2000,
			duration: 1000
	})
</script>

<style lang="scss">
	.uni-margin-wrap{
		padding: 6px;
		.swiper{
			border-radius: 4px;
			overflow: hidden;
			.swiper-item{
				width: 100%;
				height: 100%;
			}
			.uni-bg-red{
				background: red;
			}
			.uni-bg-green{
				background: green;
			}
			.uni-bg-blue{
				background: blue;
			}
		}
	}
	.fish-grip{
		margin-top: 12upx;
		.grip-box{
			display: flex;
			width: 100%;
			height: 100%;
			align-items: center;
			justify-content: center;
		}
	}
	.fish-card{
		display: flex;
		gap: 20upx;
		height: 240upx;
		padding: 20upx;
		box-sizing: border-box;
		border: 1px solid #ccc;
		border-radius: 6upx;
		&-left{
			width: 200upx;
			height: 200upx;
			background: red;
			
		}
		&-right{
			flex: 1;
			.top{
				.tittle{
					font-weight: 600;
				}
				.integral{
					color: #ccc;
					font-size: 12px;
					margin-left: 20upx;
				}
			}
			.mid{
				margin-top: 20upx;
				display: flex;
				justify-content: space-between;
				color: #ccc;
				font-size: 12px;
				text+text{
					margin-left: 20upx;
				}
			}
			.bottom{
				margin-top: 33upx;
			}
		}
	}
</style>