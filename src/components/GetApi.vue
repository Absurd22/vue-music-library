<template>
  <div>
    <input v-model="qurey" @keyup.enter="getMusic"/>
  </div>
</template>

<script>
import axios from 'axios';
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
export default {
  data(){
    return {
      qurey:'五月天',
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
