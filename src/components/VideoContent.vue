<template>
  <div id="videoContent">
    <button @click="getMusic">测试</button>
  </div>
</template>

<script>
import axios from 'axios';
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
