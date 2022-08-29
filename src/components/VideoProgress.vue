<template>
  <div>
    <button @click="getMusic">测试</button>
  </div>
</template>

<script>
import axios from 'axios';
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
export default {
  data(){
    return {
      qurey:'',
      musicList:[]
    }

  },
  methods:{
    getMusic:function(){
      axios.get('https://autumnfish.cn/search?keywords='+this.qurey).then((res)=>{console.log(res)})
    }
  }
}
</script>
