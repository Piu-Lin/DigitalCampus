<script setup>
import { ref } from 'vue'
import AssetManage from "./AssetManage.vue"
import MonitoringCenter from './MonitoringCenter.vue';
import OperationManagement from './OperationManagement.vue';
import Connectpxy from "./connectpxy.vue"
let subChosen = ref(1)
function switchSubChosen(v) {
    subChosen.value = v
}
function getTime(){
    var currentTime = new Date();
    var year = currentTime.getFullYear();
    var month = currentTime.getMonth() + 1;
    var day = currentTime.getDate();
    var hours = currentTime.getHours();
    var minutes = currentTime.getMinutes();
    hours = hours < 10 ? "0" + hours : hours;
    minutes = minutes < 10 ? "0" + minutes : minutes;
    var dateString = year + "年" + month + "月" + day +"日";
    var timeString = hours + ":" + minutes;
    document.getElementById("TimeData").innerHTML = dateString;
    document.getElementById("datedata").innerHTML = timeString;
}
setInterval(getTime,100);
</script>

<template>
    
    <div class="all">
        <!-- <div id="building">
        </div> -->
        <img id="baseBG" src="/pngs/baseBG.png" />
        <Connectpxy/>
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
