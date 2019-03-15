<template>
  <div class="hello">
    <h1>{{msg}}</h1>
    <button @click='bus'>兄弟们，跟你们说件事儿</button>
  </div>
</template>

<script>
import Bus from '@/bus.js'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  mounted() {
    console.log('home组件调用时，传递过来的参数',this.msg)
    this.sendOutput()
  },
  methods: {
    sendOutput() {
      this.$emit('setMsg','我已经成功的被你调用啦')
    },
    bus() {
      Bus.$emit('msg', '兄弟们，你们好，my name is HelloWorld')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
h3
  margin 40px 0 0

ul
  list-style-type none
  padding 0

li
  display inline-block
  margin 0 10px

a
  color #42b983
</style>
