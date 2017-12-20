<template>
  <div class="radio">
    <ul class="radio-list">
      <li v-for="(item,index) in selections">{{item.label}}</li>
    </ul>
  </div>
</template>

<script type="text/ecmascript-6">
  export default{
    props: {
      selections: {
        type: Array,
        default:[{
          label: 'test',
          value: 0
        }]
      }
    },
    data(){
      return{

      }
    }
  }
</script>

<style>
</style>
