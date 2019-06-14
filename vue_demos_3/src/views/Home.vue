<template>
	<div class="home">
		<img alt="Vue logo" src="../assets/logo.png">
		<HelloWorld msg="Welcome to Your Vue.js App"/>
		<p>方式1.path</p>
		<button @click='goToAbout'>path利用js事件传递路由参数</button>
		<br>
		<router-link :to="{path:'/about',query:{code:'1'}}">path利用router-link传递路由参数</router-link>
		<p>方式2.name</p>
		<button @click='namegoToAbout'>name利用js事件传递路由参数</button>
		<br>
		<router-link :to="{name:'about',params:{code:'2'}}">name利用router-link传递路由参数</router-link>
		<div>
			<p v-text='test'></p>
			<p v-html='test'></p>
		</div>
		<input type="text" v-model='inputValue'>
		<input type="checkbox" v-model='inputChecked'>
		<ul>
			<li v-for='(item,index) in dataList'>内容是：{{item}}---下标是：{{index}}</li>
		</ul>
	</div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
	name: 'home',
	components: {
		HelloWorld
	},
	data() {
		return {
			test:'<p>this is p</p>',
			inputValue:'123',
			inputChecked:true,
			dataList:[1,2,3]
		}
	},
	methods: {
		goToAbout() {
			this.$router.push({
				path:'/about',
				query:{
					code:'1'
				}
			})
		},
		namegoToAbout() {
			this.$router.push({
				name:'about',
				params:{
					code:'2'
				}
			})
		}
   }
}
</script>
