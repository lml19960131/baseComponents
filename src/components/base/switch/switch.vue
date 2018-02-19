<template>
  <label class="switch">
    <input class="switch-input" :disabled="disabled" @change="$emit('change', currentValue)" type="checkbox" v-model="currentValue">
    <span class="switch-core"></span>
    <div class="switch-label">
      <slot></slot>
    </div>
  </label>
</template>

<script type="text/ecmascript-6">
  export default {
    name: 'mt-switch',
    props: {
      value: Boolean,
      disabled: {
        type: Boolean,
        default: false
      }
    },
    computed: {
      currentValue: {
        get() {
          return this.value;
        },
        set(val) {
          this.$emit('input', val);
        }
      }
    }
  };
</script>

<style scoped lang='stylus' rel="stylesheet/stylus">
  .switch
    display flex
    align-items center
    position relative

</style>
