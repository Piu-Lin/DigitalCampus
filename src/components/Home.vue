<script setup>
import { ref } from 'vue'
let subChosen=ref(1)
function switchSubChosen(v){
    subChosen.value=v
}
</script>

<template>
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
    <div id="leftPanel">
        <img class="panelBg" src="/pngs/PanelBG.png"/>
        <div class="panelContent">
        </div>
    </div>
    <div id="rightPanel">
        <img class="panelBg" src="/pngs/PanelBG.png"/>
    </div>
  </div>
</template>

<style scoped>
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
    left: 30vw;
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
    font-size: 1。1rem;
}
#leftPanel{
    position: absolute;
    width: 20vw;
    height: 91vh;
    top:9vh;
    left: 0px;
}
.panelBg{
    width: 20vw;
    height: 90vh;
    left: 0px;;
}
.panelContent{
    position: absolute;
    z-index: 10;
    color: white;
    top:0vh;
}
#rightPanel{
    position: absolute;
    width: 20vw;
    height: 91vh;
    top:9vh;
    right: 0px;
}
</style>
