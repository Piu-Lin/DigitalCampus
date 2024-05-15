<script setup>
import { ref } from 'vue'
import AssetManage from "./AssetManage.vue"
import MonitoringCenter from './MonitoringCenter.vue';
import OperationManagement from './OperationManagement.vue';
import Connectpxy from "./connectpxy.vue"
let subChosen = ref(1)
let shouldShowVideo=ref(false)
let shouldShowButton=ref(false)
let videoSource=ref('https://media.w3.org/2010/05/sintel/trailer.mp4') // 视频文件的路径
function switchSubChosen(v) {
    subChosen.value = v
}
function getTime(){
    var currentTime = new Date();
    var year = currentTime.getFullYear();
    var month = currentTime.getMonth();
    var day = currentTime.getDay();
    var hours = currentTime.getHours();
    var minutes = currentTime.getMinutes();
    hours = hours < 10 ? "0" + hours : hours;
    minutes = minutes < 10 ? "0" + minutes : minutes;
    var dateString = year + "年 " + month + "月 " + day +"日";
    var timeString = hours + ":" + minutes;
    document.getElementById("TimeData").innerHTML = dateString;
    document.getElementById("datedata").innerHTML = timeString;
}
// getTime();
setInterval(getTime,1000);
let event_name
let uemeg, meg
const trigger = (meg) => {
    console.log(meg)
    uemeg = JSON.parse(meg)
    let keys = Object.keys(uemeg)
    if(keys == "event_name"){
        event_name = uemeg.event_name
        if(event_name == "scene_display") subChosen.value = 1
        else if(event_name == "asset_management") subChosen.value = 2
        else if(event_name == "operation_management") subChosen.value = 3
        else if(event_name == "monitoring_center") subChosen.value = 4
    }
    else {
        shouldShowVideo.value = true
        shouldShowButton.value = true
        //videoSource.value = 'https://upos-hz-mirrorks3u.acgvideo.com/upgcxcode/90/65/122426590/122426590-1-6.mp4?e=ig8euxZM2rNcNbuVhwdVtWuVhwdVNEVEuCIv29hEn0l5QK==&uipk=5&nbs=1&deadline=1570938144&gen=playurl&os=ks3u&oi=3742040479&trid=06d1dfd471d34b8eb40c4cee6c79531ah&platform=html5&upsig=904b08c9cd9418a8acfd4384c8b05a30&uparams=e,uipk,nbs,deadline,gen,os,oi,trid,platform&mid=0'
    }//else if(event_name == "")
}

function toggleVideoDisplay() {
    shouldShowVideo.value = false // 切换视频显示状态
    shouldShowButton.value = false
}
</script>

<template>
    <div class="all">
        <!-- <div id="building">
        </div> -->
        <img id="baseBG" src="/pngs/baseBG.png" />
        <Connectpxy @trigger="trigger" />
        
        <div class = "videomasks">
            <!-- 视频元素，通过v-if控制显示 -->
            <video v-if="shouldShowVideo" controls autoplay width = 100% height = "100%">
            <source :src="videoSource" type="video/mp4">
            您的浏览器不支持视频播放。
            </video>
            <!-- 控制显示视频的按钮 -->
            <button v-if="shouldShowButton" @click="toggleVideoDisplay()">{{ "隐藏视频" }}</button>
        </div>
<!-- 
        <div class="videomasks" v-if="showVideo" id="app">
            <button @click="showVideo = !showVideo">切换视频显示</button>
            <video src="https://media.w3.org/2010/05/sintel/trailer.mp4" controls="controls" autoplay width="100%" height="100%"></video>
        </div> -->

        <div>
            <img id="titleBoxBG" src="/pngs/TitleBoxBG.png" />
            <div id="titleContent">之江学院数字孪生校园</div>
            <img id="titleShader" src="/pngs/TitleShader.png" />
            <div id="subTitleBox">
                <div @click="switchSubChosen(1)" class="subTitleItemBox">
                    <span class="subTitleContent">场景展示</span>
                    <img v-if="subChosen == 1" class="subTitleShader" src="/pngs/SubTitleShader.png" />
                </div>
                <div @click="switchSubChosen(2)" class="subTitleItemBox">
                    <span class="subTitleContent">资产管理</span>
                    <img v-if="subChosen == 2" class="subTitleShader" src="/pngs/SubTitleShader.png" />
                </div>
                <div @click="switchSubChosen(3)" class="subTitleItemBox">
                    <span class="subTitleContent">运营管理</span>
                    <img v-if="subChosen == 3" class="subTitleShader" src="/pngs/SubTitleShader.png" />
                </div>
                <div @click="switchSubChosen(4)" class="subTitleItemBox">
                    <span class="subTitleContent">监控中心</span>
                    <img v-if="subChosen == 4" class="subTitleShader" src="/pngs/SubTitleShader.png" />
                </div>
            </div>
            <div class="TimeDateBox">
                <span id="TimeData"></span>
                <span class="fengef">｜</span>
                <span id="datedata"></span>
            </div>

        </div>
        <AssetManage v-if="subChosen == 2" />
        <OperationManagement v-if="subChosen == 3" />
        <MonitoringCenter v-if="subChosen == 4" />
    </div>
    
</template>

<style scoped>

.videomasks {
  max-width: 120vw;
  position: absolute;
  right: 25vw;
  left: 25.vw;
  top: 80vh;
  margin-top: -30%;
  z-index: 20;
  /* transform: translate(-50%, -50%); */
}

.all {
    position: absolute;
    width: 100%;
    height: 100%;
    left: 0px;
    top: 0px;
    overflow-x: hidden;
    overflow-y: hidden;
}

#building {
    background: url("D:\\Downloads\\managementstore.png");
    width: 100%;
    height: 100%;
    position: fixed;
    background-size: 100% 100%;
}

#baseBG {
    position: absolute;
    top: 0px;
    left: 0px;
    height: 100%;
    width: 100%;
}

#titleBoxBG {
    position: absolute;
    top: 0px;
    left: 0px;
    width: 100%;
}

#titleContent {
    position: absolute;
    top: 1vh;
    left: 4vw;
    font-family: IQYHT, IQYHT;
    font-weight: bold;
    font-size: 1.5rem;
    color: white;
}

#titleShader {
    position: absolute;
    top: 0px;
    left: 0px;
    width: 30%;

}

#subTitleBox {
    position: absolute;
    top: 0px;
    height: 6vh;
    left: 23vw;
    display: flex;
}

.subTitleItemBox {
    height: 6vh;
    width: 13vw;
    position: relative;
    cursor: pointer;
}

.subTitleShader {
    height: 6vh;
}

.subTitleContent {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-30%, -20%);
    font-size: 1.1rem;
    color: white;
}

.TimeDateBox {
    position: absolute;
    top: 2vh;
    right: 5vw;
    font-size: 1.1rem;
    color: white;
}

.TimeData {
    font-weight: Bold;
    color: #CDD6E3;
}

.fengef {
    color: #F3D127;
}

.datedata {
    color: #CDD6E3;
    font-size: 0.9rem;
}
</style>
