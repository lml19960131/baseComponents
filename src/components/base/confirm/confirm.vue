<template>
  <transition name="confirm-fade">
    <div class="confirm" v-show="showFlag" @click.stop>
      <div class="confirm-wrapper">
        <div class="confirm-content">
          <p class="text">{{text}}</p>
          <div class="operate">
            <div class="operate-btn left" @click="sure">{{sureBtn}}</div>
            <div class="operate-btn right" @click="cancel">{{cancelBtn}}</div>
          </div>
        </div>
      </div>
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
      showFlag: {
        type: Boolean,
        default: false
      },
      text: {
        type: String,
        default: '删除'
      },
      sureBtn: {
        type: String,
        default: '确认'
      },
      cancelBtn: {
        type: String,
        default: '取消'
      }
    },
    methods: {
      show() {
        this.showFlag = true;
      },
      hide() {
        this.showFlag = false;
      },
      sure() {
        this.hide();
        this.$emit('sure');
      },
      cancel() {
        this.hide();
        this.$emit('cancel');
      }
    }
  }
</script>

<style scoped lang='stylus' rel="stylesheet/stylus">
  .confirm
    position fixed
    top 0
    right 0
    bottom 0
    left 0
    z-index 998
    background-color gray
      &.confirm-fade-enter-active
        animation confirm-fadein 0.3s
        .confirm-content
          animation confirm-zoom 0.3s
    .confirm-wrapper
      position absolute
      top 50%
      left 50%
      transform translate(-50%, -50%)
      z-index 999
      .confirm-content
        width 270px
        border-radius 13px
        background-color grey
        .text
          padding 19px 15px
          line-height 22px
          text-align center
          font-size 16px
          color white
        .operate
          display flex
          align-items center
          text-align center
          font-size 16px
          .operate-btn
            flex 1
            line-height 22px
            padding 10px 0
            border-top 1px solid black
            color white
            &.left
              border-right 1px solid black



  @keyframes confirm-fadein
    0%
      opacity: 0
    100%
      opacity: 1
  @keyframes confirm-zoom
    0%
      transform: scale(0)
    50%
      transform: scale(1.1)
    100%
      transform: scale(1)
</style>
