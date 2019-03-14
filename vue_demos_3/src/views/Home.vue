<template>
	<div class="home">
		<img alt="Vue logo" src="../assets/logo.png" @click='goToAbout'>
		<HelloWorld msg="Welcome to Your Vue.js App"/>
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
			this.$router.push('/about/1')
		}
	}
}
</script>
