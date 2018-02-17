<template>
  <div class="loading" v-show="showFlag">
    <img class="loading-img" src="../../../../src/components/base/loading/loading.gif">
    <P class="desc">{{title}}</P>
  </div>
</template>

<script type="text/ecmascript-6">
  export default{
    props: {
      showFlag: {
        type: Boolean,
        default: false
      },
      title: {
        type: String,
        default: '正在载入'
      }
    }
  }
</script>

<style scoped lang='stylus' rel="stylesheet/stylus">
  .loading
    width 100%
    text-align center
    .loading-img
      width 24px
      height 24px
    .desc
      line-height 20px
      font-size 12px
      color: grey
</style>
