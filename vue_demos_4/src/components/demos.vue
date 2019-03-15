<template>
	<div>
		This is demos
	</div>
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
	},
	methods: {

	}
}
</script>
