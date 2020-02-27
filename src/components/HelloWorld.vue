<template>
  <div class="hello"  @click="getslot">
    {{msg}}
    <demo1 @showCityName="cons" ref="test" msg="测试Prop">
      <div slot="left">测试</div>
    </demo1>
  </div>
</template>

<script>
import demo1 from '@/components/demo1';
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components:{
    demo1
  },
  methods:{
    cons(val){
      console.log(val.name);
      
    },
    getslot(){
      this.$refs.test.getSlot();
      // console.log(this);
      
    }
  },
  created:function(){
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
