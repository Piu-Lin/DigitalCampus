<script setup>
import { ref } from 'vue'

</script>

<template>
    <div>
        
    </div>
    <div id="leftPanel">
        <img class="panelBg" src="/pngs/PanelBG.png"/>
        <div class="panelContent">
            资产管理
        </div>
        <div>
            资产管理111
        </div>
    </div>
                                    
    <div id="rightPanel">
        <img class="panelBg" src="/pngs/PanelBG.png"/>
        <div class="panelContent">
            
        </div>
    </div>
</template>

<style scoped>
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
