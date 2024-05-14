<script setup>
import { ref } from 'vue'
import AssetManage from "./AssetManage.vue"
let subChosen=ref(1)
function switchSubChosen(v){
    subChosen.value=v
}
</script>

<template>
    <div id="building">
    </div>
  <div>
    <img id="baseBG" src="/pngs/baseBG.png"/>
    <img id="titleBoxBG" src="/pngs/TitleBoxBG.png"/>
    <div id="titleContent">之江学院数字孪生校园</div>
    <img id="titleShader" src="/pngs/TitleShader.png"/>
    <div id="subTitleBox">

        <div @click="switchSubChosen(1)" class="subTitleItemBox" >
            <span class="subTitleContent">场景展示</span>
            <img  v-if="subChosen==1"  class="subTitleShader" src="/pngs/SubTitleShader.png"/>
        </div>
        <div @click="switchSubChosen(2)" class="subTitleItemBox" >
            <span class="subTitleContent">资产管理</span>
            <img v-if="subChosen==2"  class="subTitleShader" src="/pngs/SubTitleShader.png"/>
        </div>
        <div @click="switchSubChosen(3)" class="subTitleItemBox" >
            <span class="subTitleContent">运营管理</span>
            <img v-if="subChosen==3"  class="subTitleShader" src="/pngs/SubTitleShader.png"/>
        </div>
        <div @click="switchSubChosen(4)" class="subTitleItemBox" >
            <span class="subTitleContent">监控中心</span>
            <img v-if="subChosen==4"  class="subTitleShader" src="/pngs/SubTitleShader.png"/>
        </div>
    </div>
    <div class="TimeDateBox">
        <span class="TimeData">14:36</span>
        <span class="fengef">｜</span>
        <span class="datedata">2024年5月9日</span></div>
        <AssetManage v-if="subChosen==2"/>
        <OperationManagement v-if="subChosen==3"/>
        <MonitoringCenter v-if="subChosen==4"/>
  </div>
</template>

<style scoped>
#building{
      background:url("D:\\Downloads\\managementstore.png");
      width:100%;			
      height:100%;			
      position:fixed;
      background-size:100% 100%;}
#baseBG{
    position: absolute;
    top:0px;
    left: 0px;
    height: 100%;
    width: 100%;
}
#titleBoxBG{
    position: absolute;
    top:0px;
    left: 0px;
    width: 100%;
}
#titleContent{
    position: absolute;
    top:1vh;
    left: 4vw;
    font-family: IQYHT, IQYHT;
    font-weight: bold;
    font-size: 1.5rem;

}
#titleShader{
    position: absolute;
    top:0px;
    left: 0px;
    width: 30%;

}
#subTitleBox{
    position: absolute;
    top:0px;
    height: 6vh;
    left: 23vw;
    display: flex;
}
.subTitleItemBox{
    height: 6vh;
    width: 13vw;
    position: relative;
    cursor: pointer;
}
.subTitleShader{
    height: 6vh;
}
.subTitleContent{
    position: absolute;
    left: 50%;
    top:50%;
    transform: translate(-30%, -20%);
    font-size: 1.1rem;
}

.TimeDateBox{
    position: absolute;
    top:2vh;
    right: 5vw;
    font-size: 1.1rem;
}
.TimeData{
    font-weight: Bold;
    color: #CDD6E3;
}
.fengef{
    color: #F3D127;
}
.datedata{
    color: #CDD6E3;
    font-size: 0.9rem;
}
</style>
