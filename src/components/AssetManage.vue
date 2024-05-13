<script setup>
import { ref } from 'vue'

</script>

<template>
    <div>
        
    </div>
    <div id="leftPanel">
        <img class="panelBg" src="/pngs/PanelBG.png"/>
        <div class="panelContent">
            <div id="container0">
                <div class="imgboxyelow box1yelow">资产管理</div>
            </div>
            <div id="container1">
                <div class="imgboxblue box1blue">楼控列表</div>
            </div>
            <div id="containerControl">
                <div class="imgboxControl box1Control"></div>
            </div>
            <div id="container2">
                <div class="imgboxblue0 box1blue0">门禁列表</div>
            </div>
            <div id="doorAccess">
                <div class="imgboxDoor box1Door"></div>
            </div>
        </div>
    </div>
                                    
    <div id="rightPanel">
        <img class="panelBg" src="/pngs/PanelBG.png"/>
        <div id="container3">
            <div class="imgboxblue box1blue">设备列表</div>
        </div>
        <div id="Use">
            <div class="imgboxuse box1use"></div>
        </div>
        <div id="dname">
            <div class="imgboxdname box1dname"></div>
        </div>
        <div id="container4">
            <div class="imgboxblue box1blue">安防列表</div>
        </div>
        <div id="last">
            <div class="imgboxlast box1dlast"></div>
        </div>
    </div>
</template>

<style scoped>
#last .imgboxlast{
    position: absolute;
    top: 33vw;
    left: 0.5vw;
    height: 21vh;
    width: 15vw;
}
#last .imgboxlast{
    color: ivory;
    background-image: url(/pngs/checkList.png);
    background-size: 15vw 21vh;
    background-repeat: no-repeat;
}
#container4 .imgboxblue{
    position: absolute;
    top: 31vw;
    left: 0.5vw;
    height:4vh;
    width: 19vw;
}
#container4 .box1blue{
    font-size: 19px;
    color: ivory;
    background-image: url(/pngs/blueBack.png);
    background-size: 19vw 4vh;
    background-repeat: no-repeat;
    text-align: left;
    padding-top: 0.3vw;
    padding-left: 1.7vw;
}

#dname .imgboxdname{
    position: absolute;
    top: 14vw;
    left: 0.5vw;
    height: 34vh;
    width: 19vw;
}
#dname .box1dname{
    color: ivory;
    background-image: url(/pngs/devicesOfTeach.png);
    background-size: 19vw 34vh;
    background-repeat: no-repeat;
}

#Use .imgboxuse{
    position: absolute;
    top: 2.4vw;
    left: 0.5vw;
    height: 23vh;
    width: 18vw;
}
#Use .box1use{
    color: ivory;
    background-image: url(/pngs/devicesOfWrong.png);
    background-size: 18vw 23vh;
    background-repeat: no-repeat;
}

#container3 .imgboxblue{
    position: absolute;
    top: 0.2vw;
    left: 0.5vw;
    height:4vh;
    width: 19vw;
}
#container3 .box1blue{
    font-size: 19px;
    color: ivory;
    background-image: url(/pngs/blueBack.png);
    background-size: 19vw 4vh;
    background-repeat: no-repeat;
    text-align: left;
    padding-top: 0.3vw;
    padding-left: 1.7vw;
}
#doorAccess .imgboxDoor{
    position: absolute;
    top: 27vw;
    left: 1vw;
    height: 32vh;
    width: 17vw;
}
#doorAccess .box1Door{
    font-size: 19px;
    color: ivory;
    background-image: url(/pngs/doorAccess.png);
    background-size: 17vw 32vh;
    background-repeat: no-repeat;
    text-align: left;
}
#container2 .imgboxblue0{
    position: absolute;
    top: 49vh;
    left: 1vh;
    height:4vh;
    width: 19vw;
}
#container2 .box1blue0{
    font-size: 19px;
    color: ivory;
    background-image: url(/pngs/blueBack.png);
    background-size: 19vw 4vh;
    background-repeat: no-repeat;
    text-align: left;
    padding-top: 0.3vw;
    padding-left: 1.7vw;
}

#containerControl .imgboxControl{
    position: absolute;
    top: 15vh;
    left: 2vh;
    height: 33vh;
    width: 18vw;
}
#containerControl .box1Control{
    font-size: 19px;
    color: ivory;
    background-image: url(/pngs/controlList.png);
    background-size: 18vw 33vh;
    background-repeat: no-repeat;
    text-align: left;
}

#container1 .imgboxblue{
    position: absolute;
    top: 10vh;
    left: 1vh;
    height:4vh;
    width: 19vw;
}
#container1 .box1blue{
    font-size: 19px;
    color: ivory;
    background-image: url(/pngs/blueBack.png);
    background-size: 19vw 4vh;
    background-repeat: no-repeat;
    text-align: left;
    padding-top: 0.3vw;
    padding-left: 1.7vw;
}

#container0 .imgboxyelow{
    position: absolute;
    top: 1vw;
    left: 0.5vw;
    height: 5vh;
    width: 19vw;
}
#container0 .box1yelow{
    font-size: 21px;
    color: ivory;
    background-image: url(/pngs/yellowBack.png);
    background-size: 19vw 5vh;
    background-repeat: no-repeat;
    text-align: left;
    padding-top: 0.3vw;
    padding-left: 1.7vw;
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
