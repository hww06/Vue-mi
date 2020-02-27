<template>
  <div>
    <h1>b1</h1>
    <div></div>
    <button @click="cs">测试非父子组件通信</button>
  </div>
</template>

<script>
import tfer from './tfer'
export default {
    data(){
        return {
          msg:"测试非父子组件传递数据"
        }
    },
    methods:{
      cs(){
        tfer.$emit("to_news",this.msg)
      }
    }
}
</script>

<style>

</style>