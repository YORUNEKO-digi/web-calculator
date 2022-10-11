<template>

  <n-card  
  style="margin-bottom: 16px ;" 
  :bordered="false"
  class="menubar"
  >
    <n-tabs
    type="line" 
    animated justify-content="space-evenly" 
    trigger="click" 
    style="height: 100%"
    size= 'large'
    pane-style=" ; width: 100%; "
    >
      <n-tab-pane name="typeinput" tab="手動輸入" class="tab-pane" >
        
      </n-tab-pane>
      <n-tab-pane name="hwtab" tab="使用手寫板" class="tab-pane" >
        <Hwtab/>
      </n-tab-pane>
      <n-tab-pane name="flieupload" tab="上傳檔案辨識" class="tab-pane"  >
        <Uploader class="Uploader"/>
      </n-tab-pane>
    </n-tabs>
  </n-card>
 
</template>

<script setup>
  import { NCard } from 'naive-ui';
  import { NTabs } from 'naive-ui';
  import { NTabPane } from 'naive-ui';
import Uploader from './uploader.vue';
import Hwtab from './hwtab.vue';
</script>
<style scoped>
  .menubar{
    width: 100%;
    height: 100%;
  }
 .Uploader{
  height: 100%;
 }
</style>

 