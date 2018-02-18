<template>
  <transition name="drop">
    <div class="top-tip" v-show="showFlag" @click.stop="hide">
      <slot></slot>
    </div>
  </transition>
</template>

<script type="text/ecmascript-6">
  export default{
    data() {
      return {
      }
    },
    props: {
      delayTime: {
        type: Number,
        default: 1000
      },
      showFlag: {
        type: Boolean,
        default: false
      }
    },
    methods: {
      hide() {
        this.showFlag = false;
      },
      show() {
        this.showFlag = true;
        clearTimeout(this.timer);
        this.timer = setTimeout(() => {
          this.hide()
        }, this.delayTime)
      }
    }
  }
</script>

<style scoped lang='stylus' rel="stylesheet/stylus">
  .top-tip
    position fixed
    top 0
    left 0
    width 100%
    height 18px
    z-index 500
    line-height 18px
    background-color gray
    font-size 14px
    color white
    &drop-enter-active, &drop-leave-active
        transition all 0.3s
    &drop-enter, &drop-leave-to
      transform translate3d(0, -100%, 0)
</style>
