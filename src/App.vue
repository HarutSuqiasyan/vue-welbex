<template>
  <div class="bg-[#0E1014]">  <!-- Container -->
    <div class="absolute left-[200px] bg-gradient-to-r from-[#FFFFFF] via-[#FFD8A0] via-[#FD8787] to-[#DBA6FF] w-[1px] h-screen rotate-180 z-20 opacity-10 ">
    </div>
    <div class="w-180 h-140 absolute top-0 left-0 backdrop-blur-[10px] z-11 max-xl:w-130 max-lg:w-130 max-lg-h-screen max-md:w-screen max-md:h-135 max-[548px]:w-screen max-[548px]:min-h-190 max-[1280px]:h-125 "></div>
    <div class="absolute top-[320px] left-[700px] w-70 h-70 bg-orange-color rounded-full blur-2xl opacity-10 shadow-2xl max-xl:left-[400px] max-lg:top-[200px] max-lg:left-[300px] max-xl:w-50 max-xl:h-50 max-sm:left-0 max-sm:top-120" ></div>
    <div class="absolute top-[100px] left-[-200px] w-100 h-100 bg-red-color rounded-full blur-2xl opacity-5 shadow-xl" ></div>
    <div class="absolute top-20 left-140 w-[83px] h-[83px] max-sm:top-150 max-sm:left-20">
      <img src="/red_ball.svg" alt="">
    </div>
    <div class="absolute top-0 left-230 w-[60px] h-[60px] max-lg:top-1/2 max-lg:left-0">
      <img src="/purple_ball.svg" alt="">
    </div>
    <div class="absolute top-150 left-180 w-[46px] h-[46px] max-xl:top-110 max-xl:left-130 max-lg:left-115 max-lg:top-110 max-sm:top-165 max-sm:left-9 max-sm:w-8 max-sm:h-8 max-[548x]:top-150 max-[548px]:left-10">
      <img src="/yellow_ball.svg" alt="">
    </div>
    <div class="absolute top-[140px] left-[235px] w-[28px] h-[28px] max-xl:hidden max-lg:top-[100px] max-lg:left-[150px] max-sm:top-[190px] max-sm:left-[120px] max-[510px]:left-10" >
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