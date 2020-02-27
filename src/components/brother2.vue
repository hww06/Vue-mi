<template>
  <div>
      <h1>b2</h1>
      <p>{{msg}}</p>
  </div>
</template>

<script>
import tfer from './tfer'
export default {
    data(){
      return{
        msg:""
      }
    },
    mounted:function(){
        tfer.$on("to_news",data=>{
        this.msg = data;
      })
    }
}
</script>

<style>

</style>