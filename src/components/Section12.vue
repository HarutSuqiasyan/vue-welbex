<template>
<div class="pt-40 pl-50 max-[1300px]:pl-15 max-[1024px]:pl-10 max-[768px]:pl-6 max-[480px]:pl-3 flex flex-col flex-wrap relative">
    <div class="absolute top-40 left-[70%]">
        <img src="/purple_ball.svg" alt="">
    </div>
    <div class="absolute top-[320px] left-[-100px] w-70 h-70 bg-orange-color rounded-full blur-2xl opacity-10 shadow-2xl"></div>
    <div>
        <h3 class="text-5xl text-light-text max-md:text-3xl max-sm:text-2xl">
            Наши клиенты
        </h3>
    </div>
    <div
        class="flex flex-wrap gap-45 pt-18 max-[1024px]:gap-20 max-[790px]:pt-12 max-[480px]:pt-6 max-[640px]:gap-8 " >
        <p
            class="text-light-text text-2xl font-medium max-[640px]:text-xl max-[480px]:text-lg"
            >
            Внедрили AmoCRM и<br/> увеличили продажи
            <span
                class="text-2xl bg-gradient-to-r from-orange-color via-[24%] to-red-color bg-clip-text text-transparent max-[640px]:text-xl max-[480px]:text-lg"
                >
             для клиентов<br/> в абсолютно разных нишах
            </span>
        </p>
        <p
            class="text-light-text text-[18px] font-light max-[640px]:text-base max-[480px]:text-sm"
            >
            Для малого, среднего и крупного<br/> бизнеса с бюджетом<br/> до 3 миллионов рублей.
        </p>
    </div>
    <div class="grid grid-cols-4 gap-7 pt-15 max-md:grid-cols-3">
        <div v-for="item in data" >
            <div class="flex flex-col text-light-text">
                <img :src="item.img" alt="" class="w-15 h-15 gap-5 max-[550px]:w-10 max-[550px]:h-10 ">
                <p class="max-[550px]:text-sm">{{ item.title }}</p>
            </div>
        </div>
    </div>
</div>
</template>
<script setup>
import {ref} from 'vue'
let data = ref([
    {
        img: '/Our-clients/клининг.svg',
        title: 'Клининг'
    },
    {
        img: '/Our-clients/консалтинг.svg',
        title: 'Консалтинг'
    },
    {
        img: '/Our-clients/логистика.svg',
        title: 'Логистика'
    },
    {
        img: '/Our-clients/маркетинг.svg',
        title: 'Маркетинг и реклама'
    },
    {
        img: '/Our-clients/недвижимость.svg',
        title: 'Недвижимость'
    },
    {
        img: '/Our-clients/образование.svg',
        title: 'Образование'
    },
    {
        img: '/Our-clients/продажи.svg',
        title: 'Продажи услуг и товаров'
    },
    {
        img: '/Our-clients/производство.svg',
        title: 'Производство'
    },
    {
        img: '/Our-clients/спорт.svg',
        title: 'Спорт и здоровье'
    },
    {
        img: '/Our-clients/строительство.svg',
        title: 'Строительство'
    },
    {
        img: '/Our-clients/транспорт.svg',
        title: 'Транспортные услуги'
    },
    {
        img: '/Our-clients/финансы.svg',
        title: 'Финансовые услуги'
    },
    {
        img: '/Our-clients/юрилические.svg',
        title: 'Юридические услуги'
    },
    {
        img: '/Our-clients/B2B.svg',
        title: 'B2B поставки'
    },
    {
        img: '/Our-clients/HR.svg',
        title: 'HR и онлайн-рекрутинг'
    },
    {
        img: '/Our-clients/IT.svg',
        title: 'IT-сфера'
    },
])
</script>