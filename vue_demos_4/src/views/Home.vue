<template>
	<div class="home">
		<img alt="Vue logo" src="../assets/logo.png" @click='goToAbout'>
		<HelloWorld msg="Welcome to Your Vue.js App" @setMsg = 'getChildMsg'/>
		<Hello/>
		<Demos/>
	</div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Hello from '@/components/Hello.vue'
import Demos from '@/components/demos.vue'
export default {
	name: 'home',
	components: {
		HelloWorld,Hello,Demos
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
		},
		getChildMsg(childMsg){
			console.log('子组件传递过来的数据为--->>>',childMsg)
		}
	}
}
</script>
