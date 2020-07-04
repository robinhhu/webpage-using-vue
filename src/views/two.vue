<template>
    <div>
    <div class="jumbotron" style="background-image:url(bg1.jpg);background-repeat: no-repeat;margin-bottom:0;background-size: 100%">
        <div style="background-color:rgba(0,0,0,0.5);padding:5vw;z-index:-100">
            <h2 align=center style="color:white; margin-top: 24vh; margin-bottom: 20vh; font-weight: bold">僵尸企业识别分类</h2>
        </div>
    </div>
        <div class="row">
            <nav>
                <div class="nav nav-tabs" id="nav-tab" role="tablist">
                    <a class="nav-item nav-link active" style="font-weight:bold;color:#669" id="nav-home-tab" data-toggle="tab" href="#nav-home" role="tab" aria-controls="nav-home" aria-selected="true">单个查询</a>
                    <a class="nav-item nav-link" style="font-weight:bold;color:#669" id="nav-profile-tab" data-toggle="tab" href="#nav-profile" role="tab" aria-controls="nav-profile" aria-selected="false">批量查询</a>
                </div>
            </nav>
        </div>
        <div class="tab-content" id="nav-tabContent">
            <div class="tab-pane fade show active" id="nav-home" role="tabpanel" aria-labelledby="nav-home-tab">
                <br/><br/>
                <div class="row">
                <div class="col-lg-4" style="margin-top:4vh">
                    <form action="upload">
                        <label for="uploads" style="font-weight: bold">点击上传文件（csv）</label>
                        <input type="file" name="uploads" multiple="multiple" id="my-file" style="margin-left:9.75vw">
                        <div><button @click="submit" style="color: #333;border: 1px solid #ddd">Submit</button></div>
                    </form>
                </div>
                <div class="col-lg-1" style="margin-top:10vh;margin-bottom: 10vh">
                    <a class="DownButtonNormal" name="DownLoadHistEvent" download="企业分类.jpg" href="企业分类.jpg">企业分析报告</a>
                </div>
                <div class="col-lg-2" style="margin-top:10vh;margin-bottom: 10vh">
                    <input type="button" @click="changeShow" class="sc" value="企业分类结果" style="padding-left: 1vw;padding-right: 1vw">
                    <p class="sc1" v-bind:class="{'showing' : isOrNot}">
                        是僵尸企业
                    </p>
                </div>
                <br/><br/>
                </div>
            </div>
            <div class="tab-pane fade show" id="nav-profile" role="tabpanel" aria-labelledby="nav-profile-tab">
                <br/><br/>
                <div class="row">
                <div class="col-lg-4" style="margin-top:4vh">
                    <form action="upload">
                        <label for="uploads" style="font-weight: bold">点击上传文件（csv）</label>
                        <input type="file" name="uploads" multiple="multiple" id="my-file" style="margin-left:9.5vw">
                        <div><button @click="submit" style="color: #333;border: 1px solid #ddd">Submit</button></div>
                    </form>
                </div>
                <div class="col-lg-1" style="margin-top:9vh;margin-bottom: 10vh">
                    <a class="DownButtonNormal" name="DownLoadHistEvent" download="企业分类结果.csv" href="企业分类结果.csv">企业分类结果</a>
                </div>
                <div class="col-lg-5" style="margin-top:10vh;margin-bottom: 10vh;padding-left: 1.5vw">
                    <select name="select" id="select" onchange="b();">
                        <option value="0" >注册时间</option>
                        <option value ="1">2000</option>
                        <option value ="2">2001</option>
                        <option value ="3">2002</option>
                        <option value ="4">2003</option>
                        <option value ="5">2004</option>
                        <option value ="6">2005</option>
                        <option value ="7">2006</option>
                        <option value ="8">2007</option>
                        <option value ="9">2008</option>
                        <option value ="10">2009</option>
                        <option value ="11">2010</option>
                        <option value ="12">2011</option>
                        <option value ="13">2012</option>
                        <option value ="14">2013</option>
                        <option value ="15">2014</option>
                    </select>
                    <select name="select" id="select" onchange="b();">
                        <option value="0" >行业</option>
                        <option value ="1">服务业</option>
                        <option value ="2">交通运输业</option>
                        <option value ="3">工业</option>
                        <option value ="4">零售业</option>
                        <option value ="5">商业服务业</option>
                        <option value ="6">社区服务</option>
                    </select>
                    <select name="select" id="select" onchange="b();">
                        <option value="0" >区域</option>
                        <option value ="1">广东</option>
                        <option value ="2">江西</option>
                        <option value ="3">山东</option>
                        <option value ="4">广西</option>
                        <option value ="5">湖南</option>
                        <option value ="6">湖北</option>
                        <option value ="7">福建</option>
                    </select>
                    <select name="select" id="select" onchange="b();">
                        <option value="0" >企业类型</option>
                        <option value ="1">股份有限公司</option>
                        <option value ="2">农民专业合作社</option>
                        <option value ="3">集体所有制企业</option>
                        <option value ="4">有限责任公司</option>
                    </select>
                    <select name="select" id="select" onchange="b();">
                        <option value="0" >控制人类型</option>
                        <option value ="1">企业法人</option>
                        <option value ="2">自然人</option>
                    </select>
                    <select name="select" id="select" onchange="b();">
                        <option value="0" >是否僵尸企业</option>
                        <option value ="1">0</option>
                        <option value ="2">1</option>
                    </select>
                </div>
                <div class="col-lg-1" style="margin-top:9vh;margin-bottom: 10vh">
                    <a class="DownButtonNormal" download="企业筛选报告.csv" href="企业筛选报告.csv">企业筛选结果</a>
                </div>
            </div>
        </div>
        </div>  
    </div>
</template>

<script>
export default {
    name: 'two',
    data () {
        return {
            isOrNot: true
        }
    },
    methods: {
        submit: function(e) {
            e.preventDefault();
        },
        changeShow: function() {
            this.isOrNot = !this.isOrNot;
        }
        // open: function(){
        //     window.location.href='../../public/alertpic.html';
        // }}
        }
    }
</script>

<style scoped>
.showing {
    display: none;
}
.DownButtonNormal {
    -webkit-appearance: push-button;
    user-select: none;
    white-space: pre;
    align-items: flex-start;
    text-align: center;
    cursor: default;
    color: black;
    font-weight: lighter;
    background-color: rgb(239, 239, 239,0.8);
    box-sizing: border-box;
    padding: 2.6px 7.25px;
    border-width: 0.5px;
    border-style: outset;
    border-color: rgb(195,195,195);
    border-image: initial;
    text-decoration: none;
}
</style>