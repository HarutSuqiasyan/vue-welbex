<template>
    <div class="pl-50 pt-25 max-[1300px]:pl-15 max-[1024px]:pl-10 max-[768px]:pl-6 max-[480px]:pl-4 flex flex-col flex-wrap relative">
        <div class="absolute top-[20%] left-[20%] w-80 h-80 bg-[#833AB4] rounded-full blur-2xl opacity-10 shadow-2xl"></div>
        <div class="absolute top-[10%] left-[80%] w-80 h-80 bg-[#961A1A] rounded-full blur-2xl opacity-10 shadow-2xl"></div>
        <div class="pb-15">
            <h3 class="text-5xl text-light-text max-md:text-3xl max-sm:text-2xl">Благодарственные письма</h3>
        </div>
        <div class="flex gap-10 max-md:flex-col">
            <div class=" order-1 flex flex-col gap-5 max-md:order-2">
                <div class="flex-flex-col">
                    <p class="text-light-text font-medium text-2xl max-[640px]:text-xl max-[480px]:text-lg">Компания  <span class="text-2xl bg-gradient-to-r from-orange-color via-[24%] to-red-color bg-clip-text text-transparent">Фильтрон</span></p>
                    <p class="text-[#656566]">Пантюшин Д.В.</p>
                </div>
                <div>
                    <p class="text-light-text text-[16px] font-light">«Над проектом работала целая команда. Всё было<br/> сделано профессионально, в согласованные сроки.<br/> Все вопросы решались. Руководитель проекта Елена<br/> всегда на связи: фиксировала информацию,<br/> организовывала всю работу своевременно.<br/> От компании Фильтрон, выражаю благодарность.<br/> Молодцы!»</p>
                </div>
                <div>
                    <p class="text-[16px] text-blue-color">Читать письмо целиком ></p>
                </div>
            </div>
            <div class="order-2 grid grid-cols-3 gap-5 max-[530px]:grid-cols-2 max-[880px]:grid-cols-2 max-md:order-1 max-md:grid-cols-4 max-sm:grid-cols-3  ">
                <div v-for="item in data" class="w-50 h-25 max-[1000px]:w-40 max-[1000px]:h-15 max-[530px]:w-30 max-[530px]:h-10 max-[425px]:w-25 max-[370px]:w-20 bg-black flex justify-center items-center">
                    <img :src="item" alt="">
                </div>
            </div>     
        </div>
    </div>
</template>
<script setup>
import {ref} from 'vue'
let data = ref(['/Section15/filtroncolor.svg','/Section15/filtrongray.svg','/Section15/sendpulse.svg','/Section15/smscenter.svg','/Section15/smscenter.svg','/Section15/ipivanov.svg','/Section15/filtrongray.svg','/Section15/filtrongray.svg','/Section15/filtrongray.svg'])
</script>