<template>
  <div class="bg-[#0E1014]">  <!-- Container -->
    <div class="absolute left-[200px] bg-gradient-to-r from-[#FFFFFF] via-[#FFD8A0] via-[#FD8787] to-[#DBA6FF] w-[1px] h-screen rotate-180 z-20 opacity-10 ">
    </div>
    <div class="w-180 h-150 absolute top0 left-0 backdrop-blur-[10px] z-11 max-xl:w-150 max-lg:w-0"></div>
    <div class="absolute top-[500px] left-[700px] w-70 h-70 bg-orange-color rounded-full blur-2xl opacity-10 shadow-2xl" ></div>
    <div class="absolute top-[230px] left-[-200px] w-100 h-100 bg-red-color rounded-full blur-2xl opacity-5 shadow-xl" ></div>
    <div class="absolute top-20 left-140 w-[83px] h-[83px]">
      <img src="/red_ball.svg" alt="">
    </div>
    <div class="absolute top-0 left-230 w-[60px] h-[60px]">
      <img src="/purple_ball.svg" alt="">
    </div>
    <div class="absolute top-150 left-180 w-[46px] h-[46px]">
      <img src="/yellow_ball.svg" alt="">
    </div>
    <div class="absolute top-140 left-235 w-[28px] h-[28px]">
      <img src="/red_ball.svg" alt="">
    </div>
    <div class="overflow-hidden">
      <Header />
      <Section1 />
    </div>
  </div>
</template>

<script setup>
import Header from './components/Header.vue'
import Section1 from './components/Section1.vue';
</script>
<style scoped>

</style>
