<template>
  <n-config-provider :theme="darkTheme" class="app">
    <Menubar/>
  </n-config-provider>
</template>
  
  <script setup>    
import { darkTheme } from 'naive-ui'
import Menubar from './components/menubar.vue';
import { NConfigProvider } from 'naive-ui'; 
// Import the functions you need from the SDKs you need
import { initializeApp } from "firebase/app";
import { getAnalytics } from "firebase/analytics";
// TODO: Add SDKs for Firebase products that you want to use
// https://firebase.google.com/docs/web/setup#available-libraries

// Your web app's Firebase configuration
// For Firebase JS SDK v7.20.0 and later, measurementId is optional
const firebaseConfig = {
  apiKey: "AIzaSyDkNyBSVxdesG66ynaysnwiOdxueQWsgkE",
  authDomain: "vue-app-37a59.firebaseapp.com",
  projectId: "vue-app-37a59",
  storageBucket: "vue-app-37a59.appspot.com",
  messagingSenderId: "243127048631",
  appId: "1:243127048631:web:f67107057efc2a0df73032",
  measurementId: "G-2Z8DKXL21G"
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);
const analytics = getAnalytics(app);
 
  </script>

<style scoped>
  .app{
    width: 100%;
    height: 100%;
  }
</style>