<template>
  <div id="container"></div>
</template>
<script setup>
import { LarkSR } from "larksr_websdk";
import {onMounted} from 'vue';
//import sendAssignMessage from "/src/tools/sendAssignMessage.js"
//import initpoint from './initpoint.json'
//import PxyCommonUI from 'pxy_webcommonui';

const sdkid="51dfc5ae3eee4301b86a49515f9c3e92"
const appid="1238132871332364288"

// const { 
//   Joystick, 
//   KJoystickEvents,
//   KJoystickSubTypes
// } = PxyCommonUI;

const emit = defineEmits(["trigger"])

onMounted(()=>{
  let larksr = new LarkSR({
    rootElement: document.getElementById('container'),
    serverAddress: "",
    authCode: sdkid,
    loadingBgUrl: 'https://www.metagis.cc:20241/loadingbg.png',
  });
  larksr.connectWithPxyHost ({
    appliId: appid
  })
  larksr.on('datachanneltext',(e)=>{
    console.log(e.data)
    emit("trigger",e.data)
  })
  window.larksr=larksr
})
</script>
<style scoped>
#joystickdom{
  position: absolute;
  left: 3vw;
  bottom: 40vh;
}
</style>