<template>
	<view class="login">
		 
		<view class="login-item">
			<view class="login-item1">
				<h3  v-show="a == true">手机号登录</h3>
				<p style="color: red;" @click="dj"  v-show="a == true">账号登录 ></p>
			</view>
			<view class="login-item2" >
				<h3 v-show="a == false">账号登录</h3>
				<p style="color: red;" @click="djl" v-show="a == false">手机号登录 ></p>
			</view>
			  
		</view>
	</view>
</template>

<script setup lang="ts">
import {ref} from 'vue'
const a = ref('false')
const dj = () =>{
	 a.value = true
		console.log(a.value);
}
const djl = () =>{
	a.value = false
	console.log(a.value);
}
</script>

<style lang="scss">
.login-item{
	display: flex;
  padding: 20rpx;		
}
.login-item1{
	display: flex
	justify-contespace-between;
	margin-top: 80rpx;
}
.login-item2{
	display: flex;
	justify-content: space-between;
	margin-top: 80rpx;
}
</style>
