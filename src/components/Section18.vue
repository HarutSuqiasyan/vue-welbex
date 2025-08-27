<template>
    <div class="pl-50 py-25 max-[1300px]:pl-15 max-[1024px]:pl-10 max-[768px]:pl-6 max-[480px]:pl-4 flex flex-col flex-wrap relative">
        <div class="pb-15">
            <h3 class="text-5xl text-light-text max-md:text-3xl max-sm:text-2xl">Вопрос/ответ</h3>
        </div>
        <div class="flex gap-60 flex-wrap max-[712px]:gap-20 relative z-20">
            <p class="text-light-text font-medium text-2xl max-[640px]:text-xl max-[480px]:text-lg">Ответы на <span class="text-2xl bg-gradient-to-r from-orange-color via-[24%] to-red-color bg-clip-text text-transparent">часто<br/> задаваемые вопросы</span></p>
            <p class="text-light-text text-[18px] font-light max-[640px]:text-base max-[480px]:text-sm">+100 полезных видео<br/> с разбором решений задач<br/> в области доработки AmoCRM.</p>
        </div>
         <div class="pt-10 w-[80%]">
            <div @click="question_1 = !question_1" class="p-5 border-1 border-[#656566] cursor-pointer group">
                <div class="flex justify-between ">
                    <p class="text-light-text text-[18px] font-light">Сколько стоит интеграция X с AmoCRM?</p>
                    <img src="/arrow_back_ios.svg" alt="" class="group-hover:rotate-270 duration-400" :class="{'group-hover:rotate-540 duration-400':question_1}">
                </div>
                <p v-if="question_1" class="text-light-text pt-3">Стоимость API интеграции с amoCRM начинается с 20000 рублей и зависит от сложности проекта. Для того, чтобы узнать точную цену, позвоните нам и запишитесь на аудит.</p>
            </div>
            <div @click="question_2 = !question_2" class="p-5 border-1 border-[#656566] cursor-pointer group">
                <div class="flex justify-between ">
                    <p class="text-light-text text-[18px] font-light">Требует ли AmoCRM обучения?</p>
                    <img src="/arrow_back_ios.svg" alt="" class="group-hover:rotate-270 duration-400" :class="{'group-hover:rotate-540 duration-400':question_2}">
                </div>
                <p v-if="question_2" class="text-light-text pt-3">Стоимость API интеграции с amoCRM начинается с 20000 рублей и зависит от сложности проекта. Для того, чтобы узнать точную цену, позвоните нам и запишитесь на аудит.</p>
            </div>
            <div @click="question_3 = !question_3" class="p-5 border-1 border-[#656566] cursor-pointer group">
                <div class="flex justify-between">
                    <p class="text-light-text text-[18px] font-light">Чем занимается Ваша компания?</p>
                    <img src="/arrow_back_ios.svg" alt="" class="group-hover:rotate-270 duration-400" :class="{'group-hover:rotate-540 duration-400':question_3}">
                </div>
                <p v-if="question_3" class="text-light-text pt-3">Стоимость API интеграции с amoCRM начинается с 20000 рублей и зависит от сложности проекта. Для того, чтобы узнать точную цену, позвоните нам и запишитесь на аудит.</p>
            </div>
         </div>
    </div>
</template>
<script setup>
import {ref} from 'vue'
let question_1 = ref(false)
let question_2 = ref(false)
let question_3 = ref(false)
</script>