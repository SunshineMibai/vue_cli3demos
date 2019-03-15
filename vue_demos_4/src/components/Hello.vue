<template>
	<div>This is Hello</div>
</template>
<script>
	import Bus from '@/bus.js'
	export default {
		data() {
			return {

			}
		},
		mounted() {
			Bus.$on('msg', (e) => {
				console.log(e)
			})
		}
	}
</script>