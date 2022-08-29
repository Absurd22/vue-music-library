<template>
  <div id="app">
    <video-header></video-header>
    <get-api></get-api>
    <video-content></video-content>

    <video-progress></video-progress>
  </div>
  
</template>

<script>
import GetApi from './components/GetApi.vue';
import VideoContent from './components/VideoContent.vue';
import VideoHeader from './components/VideoHeader.vue';
export default {
  name: 'app',
  components: {
    GetApi,
    VideoContent,
    VideoHeader
  }
}

</script>
<style lang="scss">
  html{
    position: relative;
    #app{
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    margin:auto;
    width: 60vw;
    height: 70vh;
    background-color: aqua;
    border-radius:7px;
    }
  }
</style>

<!-- 搜索歌曲的api：https://autumnfish.cn/search -->
<!-- 获取歌曲封面的api：https://autumnfish.cn/song/detail -->
