<template>
	<div class="about">
		<router-link to="/">返回Home页</router-link>
		<h1>This is an about page</h1>
	</div>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		mounted() {
			console.log(1111)
			// console.log('方式1.path方式接受参数',this.$route.query.code)
			console.log(this.$route.params.code)
		}
	}
</script>
