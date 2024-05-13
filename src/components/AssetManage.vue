<script setup>
import { ref } from 'vue'

</script>

<template>
   <div id="leftPanel">
        <img class="panelBg" src="/pngs/PanelBG.png"/>
        <div class="panelContent">
        </div>
    </div>
                                    
    <div id="rightPanel">
        <img class="panelBg" src="/pngs/PanelBG.png"/>
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
