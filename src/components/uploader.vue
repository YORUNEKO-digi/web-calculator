<template>

  <n-upload
  multiple
  directory-dnd
  action="./img"
  :max="1"
  style="height: 900px"
  accept=".jpg, .jpeg"
  id="upload-file"
  :on-change="uploadChange"
  >
  <n-upload-dragger  style="height: 750px; width: 75%; margin-left: auto; margin-right: auto;">
    <div style=" position: relative; top: 35%; width: 100%; ">
      <div style="margin-bottom: 20px">
        <n-icon size="60" :depth="9">
          <archive-icon />
        </n-icon>
      </div>
      <n-text style="font-size: 20px">
        點擊或拖曳以上傳檔案(僅接受 .jpg 及 .jpeg 檔)
      </n-text>
      <n-p depth="5" style="margin: 20px 0 0 0;">
        請不要上傳任何含有個人資訊的資料、銀行卡號、密碼、信用卡號有效期等...
      </n-p>
    </div>
  </n-upload-dragger>
  </n-upload>
</template>

<script setup>
  import { NUpload } from 'naive-ui';
  import { NUploadDragger } from 'naive-ui';
  import { NIcon } from 'naive-ui';
  import { NText } from 'naive-ui';
  import { NP } from 'naive-ui';
  import { ArchiveOutline as ArchiveIcon } from "@vicons/ionicons5";
  const uploadChange = (options) => {
    console.log(options.file);
  };
  
  


</script>



