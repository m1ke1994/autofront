
<script setup>
/* import { createRouter, createWebHistory } from 'vue-router'; */
import HeaderApp from './components/HeaderApp.vue';
import AsideMenu from './components/AsideMenu.vue';
import MainContent from './components/MainContent.vue';       
import { ref, onMounted, onUnmounted } from 'vue';
</script>
<template>
  <div class="w-full h-full">
      <div id="conteiner">
       <HeaderApp />
    </div>
     <hr class="border-2 border-[#2D3648]">
    <div id="conteiner" class="flex pt-10 h-full gap-4">
        <aside class="w-[40%]">
          <AsideMenu></AsideMenu>
        </aside>
        <div class="w-[100%]">
            <MainContent></MainContent>
        </div>
    </div>
  </div>
    
   
    
</template>




<style scoped>

</style>