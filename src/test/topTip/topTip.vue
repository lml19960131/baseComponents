<template>
  <div>
    <button @click="showTopTip">click me</button>
    <top-tip ref="topTip" :showFlag="false" delayTime="1000">
      <span>命令被执行</span>
    </top-tip>
  </div>
</template>

<script type="text/ecmascript-6">
 import TopTip from '../../components/base/topTip/topTip.vue'

  export default{
    components: {
      TopTip
    },
    methods:{
      showTopTip() {
        this.$refs.topTip.show();
      }
    }
  }
</script>

<style scoped lang='stylus' rel="stylesheet/stylus">

</style>
