<template>
  <div>
    <p>{{text}}</p>
    <button @click="showConfirm">全部删除</button>
    <confirm text="是否全部删除" sureBtn="确定" cancelBtn="取消" :showFlag="false"
             @sure="confirmClear" @cancel="hideConfirm"
             ref="confirm"></confirm>
  </div>
</template>

<script type="text/ecmascript-6">
  import Confirm from '../../components/base/confirm/confirm.vue'
  export default{
    data() {
      return {
        text: '我将要被删除'
      }
    },
    components: {
      Confirm
    },
    methods: {
      showConfirm() {
        this.$refs.confirm.show();
      },
      hideConfirm() {
        this.$refs.confirm.hide();
      },
      confirmClear() {
        this.text = '';
        this.$refs.confirm.hide();
      }
    }
  }
</script>

<style>

</style>
