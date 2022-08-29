<template>
  <div id="videoHeader">

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

<style lang="scss" scoped>
  #videoHeader{
    width: 100%;
    height: 10%;
    border-radius: 7px 7px 0 0;
    background-color: blue;
  }
</style>
