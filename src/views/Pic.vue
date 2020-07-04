<template>
  <div class="pic">
    <div class="jumbotron" style="background-image:url(bg1.jpg);background-repeat: no-repeat;margin-bottom:0;background-size: 100%">
      <div style="background-color:rgba(0,0,0,0.5);padding:5vw;z-index:-100">
      <h2 align=center style="color:white; margin-top: 10vh; margin-bottom: 4vh; font-weight: bold">构建企业全息画像</h2>
    <!-- </div> -->
    <!-- <div class="jumbotron" style="background-color:#669; margin-bottom: 0vh"> -->
      <div class="row" style="margin-bottom: 0vh">
        <div class="col-lg-3"></div>
        <div class="col-lg-7">
          <form action="upload" style="color: white">
            <label for="uploads" style="font-weight: bold;margin-bottom: 1vh">点击上传文件（csv）</label>
            <input type="file" name="uploads" multiple="multiple" id="my-file">
            <div><button @click="submit" style="color: #333;border: 1px solid #ddd;margin-left: 0.6vw;margin-bottom:3vh">Submit</button></div>
          </form>
        </div>
      </div>
      <div class="row" style="margin-bottom:10vh">
        <div class="col-lg-4"></div>
        <div class="col-lg-4">
          <div class="input-group flex-nowrap" style="margin-left: 0.7vw">
            <div class="input-group-prepend">
              <span class="input-group-text" id="addon-wrapping">
                <svg width="1em" height="1em" viewBox="0 0 16 16" class="bi bi-search" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                  <path fill-rule="evenodd" d="M10.442 10.442a1 1 0 0 1 1.415 0l3.85 3.85a1 1 0 0 1-1.414 1.415l-3.85-3.85a1 1 0 0 1 0-1.415z"/>
                  <path fill-rule="evenodd" d="M6.5 12a5.5 5.5 0 1 0 0-11 5.5 5.5 0 0 0 0 11zM13 6.5a6.5 6.5 0 1 1-13 0 6.5 6.5 0 0 1 13 0z"/>
                </svg>
              </span>
            </div>
            <input type="text" class="form-control" placeholder="输入企业ID" aria-label="Username" aria-describedby="addon-wrapping">
          </div>
        </div>
      </div>
    <!-- </div> -->
    </div>
    </div>
    <div class="row">
      <nav>
        <div class="nav nav-tabs" id="nav-tab" role="tablist">
          <a class="nav-item nav-link active" style="font-weight:bold;color:#669" id="nav-home-tab" data-toggle="tab" href="#nav-home" role="tab" aria-controls="nav-home" aria-selected="true">企业画像</a>
          <a class="nav-item nav-link" style="font-weight:bold;color:#669" id="nav-profile-tab" data-toggle="tab" href="#nav-profile" role="tab" aria-controls="nav-profile" aria-selected="false">基本信息</a>
          <a class="nav-item nav-link" style="font-weight:bold;color:#669" id="nav-contact-tab" data-toggle="tab" href="#nav-con" role="tab" aria-controls="nav-con" aria-selected="false">运营风险</a>
          <a class="nav-item nav-link" style="font-weight:bold;color:#669" id="nav-contact-tab" data-toggle="tab" href="#nav-contact" role="tab" aria-controls="nav-contact" aria-selected="false">知识产权</a>
        </div>
      </nav>
    </div>
      <div class="tab-content" id="nav-tabContent">
        <div class="tab-pane fade show active" id="nav-home" role="tabpanel" aria-labelledby="nav-home-tab">
          <div class="card panel-default">
            <div class="card-header" style="font-weight:bold;color:#669">&nbsp;&nbsp;&nbsp;企业画像</div>
            <div class="col-md-3 col-lg-3" style="margin-left: 37vw ">
            <br /><br /><br /><br />
            <img src="../../img/企业画像.png" style="margin-bottom: 10vh">
            <br /><br /><br /><br />
            </div>
          </div>
        </div>
        <div class="tab-pane fade" id="nav-profile" role="tabpanel" aria-labelledby="nav-profile-tab">
          <div class="card panel-default">
            <div class="card-header" style="font-weight:bold;color:#669">基本信息</div>
            <table class="table" style="margin-bottom: 10vh">
              <tbody>
                <tr>
                  <th>企业ID</th>
                  <td>906489</td>
                  <th>注册时间</th>
                  <td>2001</td>
                </tr>
                <tr>
                  <th>注册资本</th>
                  <td>910</td>
                  <th>行业</th>
                  <td>服务员</td>
                </tr>
                <tr>
                  <th>区域</th>
                  <td>广西省</td>
                  <th>企业类型</th>
                  <td>合伙企业</td>
                </tr>
                <tr>
                  <th>控制人类型</th>
                  <td>企业法人</td>
                  <th>控制人持股</th>
                  <td>0.67</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
        <div class="tab-pane fade" id="nav-con" role="tabpanel" aria-labelledby="nav-con-tab">
          <div class="card panel-default">
            <div class="card-header" style="font-weight:bold;color:#669">   &nbsp;&nbsp;&nbsp;运营风险</div>
            <div class="col-md-3 col-lg-3" style="margin-left: 37vw ">
              <br /><br />
              <img src="../../img/营业能力分布图.png"/>
              <br /><br /><br /><br />
            </div>
          </div>
          <div class="col-xs-12 col-sm-12">
            <div class="card panel-default">
              <div class="card-header">各标签值</div>
              <table class="table">
                <thead>
                  <tr>
                    <th>年份</th>
                    <th>从业人数</th>
                    <th>资产总额</th>
                    <th>负债总额</th>
                    <th>融资规模</th>
                    <th>营业总收入</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td>2015</td>
                    <td>61</td>
                    <td>63700</td>
                    <td>94185</td>
                    <td>3822</td>
                    <td>38220</td>
                  </tr>
                  <tr>
                    <td>2016</td>
                    <td>312</td>
                    <td>68250</td>
                    <td>33670</td>
                    <td>6825</td>
                    <td>88725</td>
                  </tr>
                  <tr>
                    <td>2017</td>
                    <td>589</td>
                    <td>72800</td>
                    <td>107835</td>
                    <td>7280</td>
                    <td>145600</td>
                  </tr>
                </tbody>
                </table>
                  <br /><br />
                <table class="table">
                  <thead>
                    <tr>
                      <th>年份</th>
                      <th>从业人数</th>
                      <th>资产总额</th>
                      <th>负债总额</th>
                      <th>融资规模</th>
                      <th>营业总收入</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <th>2015</th>
                      <td>15288</td>
                      <td>19110</td>
                      <td>-3288</td>
                      <td>0</td>
                      <td>-30485</td>
                    </tr>
                    <tr>
                      <th>2016</th>
                      <td>35490</td>
                      <td>8872.5</td>
                      <td>-9560</td>
                      <td>0</td>
                      <td>34580</td>
                    </tr>
                    <tr>
                      <th>2017</th>
                      <td>55420</td>
                      <td>14560</td>
                      <td>-14560</td>
                      <td>0</td>
                      <td>-35035</td>
                    </tr>
                  </tbody>
                </table>
            </div>
          </div>
          <div class="row" style="margin:0">
          <div class="col-lg-6" style="padding-right: 0">
            <div class="card panel-default">
              <div class="card-header">   &nbsp;&nbsp;&nbsp;企业负债率</div>
                <br />
                <img src="../../img/负债率.png" style="margin-bottom: 5vh;width: 25vw;margin-left: 11vw"/>
                <img src="../../img/负债率折线图.png" style="margin-bottom: 5vh;width: 25vw;margin-left: 11vw"/>
            </div>
          </div>
          <div class="col-lg-6" style="padding-left: 0">
            <div class="card panel-default">
              <div class="card-header">   &nbsp;&nbsp;&nbsp;企业营业总收入</div>
                <br />
                <img src="../../img/营业总收入.png" style="margin-bottom: 5vh;width: 25vw;margin-left: 11vw"/>
                <img src="../../img/营业总收入折线图.png" style="margin-bottom: 5vh;width: 25vw;margin-left: 11vw"/>
            </div>
          </div>
          </div>
          <div class="row" style="margin:0">
          <div class="col-lg-6" style="padding-right: 0">
            <div class="card panel-default">
              <div class="card-header">   &nbsp;&nbsp;&nbsp;企业利润总额</div>
                <br />
                <img src="../../img/利润总额.png" style="margin-bottom: 5vh;width: 25vw;margin-left: 11vw"/>
                <img src="../../img/利润总额折线图.png" style="margin-bottom: 5vh;width: 25vw;margin-left: 11vw"/>
            </div>
          </div>
          <div class="col-lg-6" style="padding-left: 0">
            <div class="card panel-default">
              <div class="card-header">   &nbsp;&nbsp;&nbsp;企业净利润</div>
                  <br />
                  <img src="../../img/净利润.png" style="margin-bottom: 5vh;width: 25vw;margin-left: 11vw"/>
                  <img src="../../img/净利润折线图.png" style="margin-bottom: 5vh;width: 25vw;margin-left: 11vw"/>
            </div>
          </div>
          </div>
          <div class="row" style="margin:0">
          <div class="col-lg-6" style="padding-right: 0">
            <div class="card panel-default">
            <div class="card-header">   &nbsp;&nbsp;&nbsp;企业纳税总额</div>
                <br />
                <img src="../../img/纳税总额.png" style="margin-bottom: 5vh;width: 25vw;margin-left: 11vw"/>
                <img src="../../img/纳税总额折线图.png" style="margin-bottom: 5vh;width: 25vw;margin-left: 11vw"/>
            </div>
          </div>
          <div class="col-lg-6" style="padding-left: 0">
            <div class="card panel-default">
              <div class="card-header">   &nbsp;&nbsp;&nbsp;企业融资总规模</div>
                <br />
                <img src="../../img/融资总规模.png" style="margin-bottom: 5vh;width: 25vw;margin-left: 11vw"/>
                <img src="../../img/融资总规模折线图.png" style="margin-bottom: 5vh;width: 25vw;margin-left: 11vw"/>
            </div>
          </div>
          </div>
        </div>
        <div class="tab-pane fade" id="nav-contact" role="tabpanel" aria-labelledby="nav-contact-tab">
          <div class="card panel-default">
            <div class="card-header" style="font-weight:bold;color:#669">&nbsp;&nbsp;&nbsp;知识产权</div>
            <table class="table" style="margin-bottom: 10vh">
              <thead>
                <tr>
                  <th>专利</th>
                  <th>商标</th>
                  <th>著作权</th>
                </tr>
              <thead/>
              <tbody>
                <tr>
                  <td>1</td>
                  <td>0</td>
                  <td>1</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'pic',
  methods: {
    submit: function(e) {
      e.preventDefault();
    }
  }
}
</script>

<style scoped>
  img {
    width: 100%;
  }
</style>