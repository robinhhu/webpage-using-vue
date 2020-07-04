<template>
  <div class="home">
    <div class="jumbotron" style="background-image:url(bg3.jpg);background-repeat: no-repeat;margin-bottom:0;background-size: 100%">
      <div style="background-color:rgba(0,0,0,0.5);padding:5vw;z-index:-100">
      <h3 align = center style="color:white; margin-top: 17vh; margin-bottom: 5vh; font-weight: bold">SEP (Simplfy Enterprise Portraits) 僵尸企业画像及分类系统</h3>
      <h5 align = center style="color:white; margin-top: 3vh; margin-bottom: 13vh; font-weight: bold">哥哥姐姐们说啥都队</h5>
    </div>
    </div>
    <div class="row" style="margin-top: 12vh">
      <div class="col-md-3 " style="margin-bottom: 10vh;margin-left: 11.5vw">
        <div class="thumbnail" v-bind:class="border">
          <img src="../../img/face.jpg" style="margin-bottom:1vh">
          <p align= center style="font-weight: bold; margin-top: 1vh">
            企业基本信息
          </p>
        </div>
      </div>
      <div class="col-md-3">
      <div class="thumbnail" v-bind:class="border">
        <img src="../../img/IBM.jpg" style="margin-bottom:1vh">
        <p align=center style="font-weight: bold; margin-top: 1vh">
          企业运营风险
        </p>
      </div>
      </div>
      <div class="col-md-3">
        <div class="thumbnail" v-bind:class="border">
          <img src="../../img/arm.jpg" style="margin-bottom:1vh">
          <p align=center style="font-weight: bold; margin-top: 1vh">
            知识产权分析
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'Home',
  data () {
    return {
      border: 'border'
    }
  }
}
</script>

<style scoped>
.border{
  border: 5px;
  border-color: white;
}

img {
  width: 100%;
}
</style>