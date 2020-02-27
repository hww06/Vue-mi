<template>
  <div class="demo1">
      <div class="lefts" v-if="$slots.left">
      <slot name="left"></slot>
      <div>{{msg}}</div>
      </div>
      <brother1></brother1>
      <brother2></brother2>
  </div>
</template>
<script>
import brother1 from './brother1'
import brother2 from './brother2'
export default {
    name:'demo1',
    data(){
        return{
            city:{name:'大连'}
        }
    },
    props:['msg'],
    methods:{
        getSlot(){
            // console.log(this.$slots);
            this.$emit('showCityName',this.city);
        }
    },
    components:{
        brother1,
        brother2
    }
}
</script>

<style>

</style>