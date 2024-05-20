<script setup>
import { ref } from 'vue'

</script>

<template>
   <div id="leftPanel">
        <img class="panelBg" src="/pngs/PanelBG.png"/>
        <div class="leftTitle">
            <img id="leftTitleImage" src="/pngs/OperationManagement/title.png"/>
            <span id="leftTitle1">运营管理</span>
        </div>
        <div class="securityMonitoring">
            <img id="smallImage01" src="/pngs/OperationManagement/smallTitle.png"/>
            <span id="leftTitle2">学院风采</span>
            <span id="YellowWord">我院教师在Advanced Fiber Materials期刊上发表高水平研究成果</span>
            <span id="wwrod1">2024-04-25   来源：理学院</span>
            <span id="wwrod2">    近期，我院理学院蒋国军副教授和温州大学薛立新教授团队联合在Advanced Fiber Materials上发表了题为“Porous structures of C-shaped polypropylene fibers and oil-absorbing performance of their spun-bond non-woven fabrics”的研究进展。该刊物最新IF为16.1，在材料科学排名21/342。我院蒋国军副教授为第一通讯作者，浙江工业大学之江学院为第一通讯单位。</span>
            <span id="wwrod3">    该工作通过热诱导相分离（TIPS）工艺，采取双组分稀释剂制备
C形多孔纺粘纤维，系统研究了稀释剂的组成和拉伸速度对亚微米
纤维孔形态及其对吸油性能的影响。基于Washburn和Escardino的
毛细管吸收模型，提出两个新概念来表征它们的吸油能力和吸收动
力学过程: 一是等效毛细管孔隙半径R0；二是动力学孔隙扭曲度......</span>
            <img id="img001" src="/pngs/OperationManagement/ResearchPic.png">
            <span id="bwrod1">查看全文   ＞＞＞</span>
            <!-- <img id="img01" src="/pngs/OperationManagement/img1.png"> -->
        </div>
        <div class="monitoringList">
            <img id="smallImage01" src="/pngs/OperationManagement/smallTitle.png"/>
            <span id="leftTitle2">人物风采</span>
            <span id="bwrod2">查看下一位   ＞＞＞</span>
            <img id="img002" src="/pngs/OperationManagement/Header.png">
            <span id="ywrod2">姜少飞</span>
            <span id="uheader">浙江工业大学之江学院院长</span>
            <span id="wwrod4">男，1975年8月生，山西大同人，博士，教授，博士生导师。
浙江工业大学学术委员会委员。2019年12月起任之江学院院长，
主持学院行政全面工作，负责审计工作，分管学院办公室(宣传部、
国际交流与合作部)。2023年12月起任浙江工业大学党委委员。
浙江省高校中青年学科带头人，浙江省151人才工程第二层次人才，
绍兴市重点科技创新团队负责人，入选绍兴市“名士之乡”......</span>
            <!-- <img id="img02" src="/pngs/OperationManagement/img2.png"> -->
        </div>
    </div>
                                    
    <div id="rightPanel">
        <img class="panelBg" src="/pngs/PanelBG.png"/>
        <div class="fireMonitoring">
            <img id="smallImage02" src="/pngs/OperationManagement/smallTitle.png"/>
            <span id="rightTitle1">教师统计</span>
            <img id="img03" src="/pngs/OperationManagement/img3.png">
        </div>
        <div class="energyMonitoring">
            <img id="smallImage02" src="/pngs/OperationManagement/smallTitle.png"/>
            <span id="rightTitle1">学生统计</span>
            <img id="img04" src="/pngs/OperationManagement/img4.png">
        </div>
        <div class="accessControl ">
            <img id="smallImage02" src="/pngs/OperationManagement/smallTitle.png"/>
            <span id="rightTitle1">门禁管理</span>
            <img id="img05" src="/pngs/OperationManagement/img5.png">
        </div>
    </div>
</template>

<style scoped>
#wwrod4{
    position: absolute;
    color: white;
    font-size: 0.58vw;
    width: 18vw;
    top: 31.8vh;
    left: 0.85vw;
    text-indent: 2em;
    text-align: justify;
}
#uheader
{
    position: absolute;
    color: white;
    width: 10vw;
    font-size: 0.55vw;
    top: 29.4vh;
    left: 5.5vw;
}
#ywrod2{
    position: absolute;
    color: #FFBB00;
    width: 7vw;
    font-size: 0.7vw;
    top: 29vh;
    left: 2.3vw;
}
#img002{
    position: absolute;
    top: 14vh;
    width: 18vw;
    left: 1vw;
}
#bwrod2{
    position: absolute;
    color: #00FFFF; 
    font-size: 0.58vw;
    width: 18vw;
    top: 12vh;
    left: 6.8vw;
}
#bwrod1{
    position: absolute;
    color: #00FFFF; 
    font-size: 0.58vw;
    width: 18vw;
    top: 48vh;
    left: 7vw;
}
#wwrod3{
    position: absolute;
    color: white;
    font-size: 0.58vw;
    width: 18vw;
    top: 38.8vh;
    left: 0.85vw;
    text-indent: 2em;
    text-align: justify;
}
#wwrod2{
    position: absolute;
    color: white;
    font-size: 0.58vw;
    width: 18vw;
    top: 28.1vh;
    left: 0.85vw;
    text-indent: 2em;
    text-align: justify;
}
#wwrod1{
    color: white;
    position: absolute;
    width: 18vw;
    font-size: 0.6vw;
    top: 14vh;
    left: 0.5vw;
}
#YellowWord{
    position: absolute;
    width: 18vw;
    color: #FFBB00;
    top: 12vh;
    left: 0.74vw;
    font-size: 0.6vw;
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
    top: 0px;
    left: 0px;
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
.securityMonitoring{
    position: absolute;
    top: 0.5vw;
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
#img001{
    position: absolute;
    top: 16vh;
    width: 18vw;
    left: 1vw;
}
#img01{
    position: absolute;
    top: 6vw;
    left: 1vw;
    width: 18vw;
}
.monitoringList{
    position: absolute;
    top: 22vw;
    left: 0vw;
}
#img02{
    position: absolute;
    top: 6vw;
    left: 1vw;
    width: 18vw;
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
.fireMonitoring{
    position: absolute;
    top: 0vw;
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
.energyMonitoring{
    position: absolute;
    top: 17vw;
    left: 0vw;
}
#img04{
    position: absolute;
    top: 4vw;
    left: 1vw;
    width: 18vw;
}
.accessControl{
    position: absolute;
    top: 29vw;
    left: 0vw;
}
#img05{
    position: absolute;
    top: 3vw;
    left: 1vw;
    width: 18vw;
}
</style>
