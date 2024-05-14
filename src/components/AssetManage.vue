<script setup>
import { ref } from 'vue'

</script>

<template>    
    <div id="leftPanel">
        <img class="panelBg" src="/pngs/PanelBG.png"/>
        <div class="leftTitle">
            <img id="leftTitleImage" src="/pngs/Management/yellowBack.png"/>
            <span id="leftTitle1">资产管理</span>
        </div>
        <div class="securityMonitoring">
            <img id="smallImage01" src="/pngs/Management/blueBack.png"/>
            <span id="leftTitle2">楼控列表</span>
            <img id="img01" src="/pngs/Management/controlList.png">
        </div>

        <div class="monitoringList">
            <img id="smallImage01" src="/pngs/Management/blueBack.png"/>
            <span id="leftTitle2">门禁列表</span>
            <img id="img02" src="/pngs/Management/doorAccess.png">
        </div>
        
    </div>
                                    
    <div id="rightPanel">
        <img class="panelBg" src="/pngs/PanelBG.png"/>
        <div class="fireMonitoring">
            <img id="smallImage02" src="/pngs/Management/blueBack.png"/>
            <span id="rightTitle1">设备列表</span>
            <img id="img03" src="/pngs/Management/devicesOfWrong.png">
            <img id="img04" src="/pngs/Management/devicesOfTeach.png">
        </div>
        <div class="energyMonitoring">
            <img id="smallImage02" src="/pngs/Management/blueBack.png"/>
            <span id="rightTitle1">安防列表</span>
            <img id="img05" src="/pngs/Management/checkList.png">
        </div>
    </div>
</template>

<style scoped>

.energyMonitoring{
    position: absolute;
    top: 31.7vw;
    left: 0vw;
}
#smallImage02{
    position: absolute;
    top: 1vw;
    left: 1.75vw;
    width: 16.75vw;
    height: 2vw;
}
#rightTitle1{
    display: flex;  
    position: absolute;
    top: 0.2vw;
    left: 4vw;
    width: 16vw;
    height: 3.5vw;
    color: white;
    font-weight: bold;
    font-size:1.75ch;
    text-align: center;
    align-items: center;
}
#img03{
    position: absolute;
    top: 4vw;
    left: 1vw;
    width: 18vw;
}
#img04{
    position: absolute;
    top: 16vw;
    left: 1vw;
    width: 18vw;
}
#img05{
    position: absolute;
    top: 3vw;
    left: 1vw;
    width: 18vw;
    height: 20.5vh;
}
.fireMonitoring{
    position: absolute;
    top: 0vw;
    left: 0vw;
}
.monitoringList{
    position: absolute;
    top: 21vw;
    left: 0vw;
}
#img02{
    position: absolute;
    top: 5.5vw;
    left: 1vw;
    height: 37vh;
    width: 18vw;
}
#img01{
    position: absolute;
    top: 6vw;
    left: 1vw;
    width: 18vw;
}
.securityMonitoring{
    position: absolute;
    top: 0vw;
    left: 0vw;
}
#smallImage01{
    position: absolute;
    top: 3.5vw;
    left: 1.75vw;
    width: 16.75vw;
    height: 2vw;
}
#leftTitle2{
    display: flex;  
    position: absolute;
    top: 2.7vw;
    left: 4vw;
    width: 17vw;
    height: 3.5vw;
    color: white;
    font-weight: bold;
    font-size:1.75ch;
    text-align: center;
    align-items: center;
}
.leftTitle{
    position: absolute;
    top: 0px;
    left: 0.75vw;
    font-weight: bold;
    text-align: center;
    align-items: center;
}

#leftTitleImage{
    position: absolute;
    top: 1vw;
    left: 0.75vw;
    width: 17vw;
    height: 3vw;
}
#leftTitle1{
    display: flex;  
    position: absolute;
    top: 0.5vw;
    left: 3vw;
    width: 17vw;
    height: 3.5vw;
    color: white;
    /* font-weight: bold; */
    font-size: larger;
    text-align: center;
    align-items: center;
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
    left: 0px;
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
