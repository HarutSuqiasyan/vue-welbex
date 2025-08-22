<template>
    <div class="pl-50 pt-36 pb-[170px] max-[1300px]:pl-15 max-[1024px]:pl-10 max-[768px]:pl-6 max-[480px]:pl-4 relative z-20">
        <div class="absolute bottom-0 left-1/2  w-6 h-6">
            <img src="/yellow_ball.svg" alt="">
        </div>
        <div class="absolute  bottom-0 left-1/2 translate-x-[-50%] w-25 h-25 bg-orange-color rounded-full blur-2xl opacity-10 shadow-5xl " ></div>
        <div class="absolute bottom-0 z-10 right-1/8">
            <img src="/dots.svg" alt="">
        </div>
        <div class="absolute bottom-0 right-1/10 w-12 h-12">
            <img src="/red_ball.svg" class="w-10 h-10" alt="">
        </div>
        <div class="">
            <div>
                <h3 class="text-5xl text-light-text max-md:text-3xl max-sm:text-2xl">Услуги</h3>
            </div>
            <div class="flex gap-40 pt-18 items-center flex-wrap max-[790px]:gap-10 max-[790px]:pt-12 max-[480px]:gap-5 max-[480px]:pt-6">
                <div>
                    <p class="text-light-text text-2xl font-medium ">Наша компания оказывает<br/><span class="bg-gradient-to-r from-orange-color via-[24%] to-red-color bg-clip-text text-transparent"> целый спектр услуг для<br/> вашего бизнеса</span></p>
                </div>
                <div>
                    <p class="text-light-text text-[18px] font-normal">От аудита отдела продаж<br/> до создания автоматизированной<br/> системы продаж.</p>
                </div>
            </div>
        </div>
        <div class="relative z-20">
            <div class="grid grid-cols-3 gap-10 pt-20 max-[1140px]:grid-cols-2 max-md:grid-cols-1 max-md:place-items-center">
                <div v-for="(item, i) in data" :key="i" class="cursor-pointer w-90 h-66 bg-gradient-to-br from-white/10 to-black rounded-lg p-5 max-[400px]:w-76 max-[400px]:h-65 max-md:h-30 relative" :class="{'max-md:h-60': item.isOpen}">
                    <div @click="openDes(i)" class="flex flex-col justify-center gap-5 relative max-[400px]:gap-3">
                        <div @click="openDes(i)" class="absolute top-3 right-0 transition-transform duration-300 md:hidden" :class="{'rotate-180': item.isOpen}">
                            <img src="/arrow_back_ios.svg" alt="">
                        </div>
                        <div class="md:hidden flex gap-2 items-center">
                            <img :src="item.icon" :alt="item.name" class="w-[70px] h-[70px]">
                            <h3 class="text-[16px] text-light-text font-normal">{{ item.name }}</h3>
                        </div>
                        <img :src="item.icon" :alt="item.name" class="w-[70px] h-[70px] max-md:hidden" :class="{'hidden':item.isOpen}">
                        <h3 class="text-[18px] text-light-text font-normal max-md:hidden">{{ item.name }}</h3>
                        <p class="text-light-text text-[16px] font-extralight md:block max-[400px]:text-[13px]" :class="{'max-md:hidden': !item.isOpen, 'max-md:block': item.isOpen }">{{ item.description }}</p>
                    </div>
                    <div class="hidden" :class="{'button_active m-5 max-md:hidden': item.isOpen}">
                        <p>Заказать услугу</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { reactive } from "vue";
const data = reactive([
    {
        icon: "icons/продажа1.svg",
        name: "Продажа лицензии",
        description: "При покупке или продлении amoCRM через нас, вы получаете  дополнительные месяцы в подарок для каждого пользователя.",
        isOpen: false 
    }, 
    {
        icon: "icons/внедрение2.svg",
        name: "Внедрение AmoCRM под ключ",
        description: "Правильно настроенная CRM-система даёт гарантированный результат и выход на новый уровень.",
        isOpen: false
    },
    {
        icon: "icons/аудитстратегия3.svg",
        name: "Аудит и стратегия",
        description: "Проведём аудит, найдём слабые места и составим стратегию развития вашей CRM-системы и отдела продаж.",
        isOpen: false
    },
    {
        icon: "icons/сопровождение4.svg",
        name: "Сопровождение, развитие, техническая помощь",
        description: "Персональный менеджер всегда на связи по любым вопросам.",
        isOpen: false
    },
    {
        icon: "icons/разработка5.svg",
        name: "Индивидуальная разработка, кастомизация, доработка",
        description: "Создадим под ваши бизнес процессы и задачи нестандартное решение в CRM-системе.",
        isOpen: false
    }, 
    {
        icon: "icons/аренда6.svg",
        name: "Аренда виджетов",
        description: "Закажите уже готовое решение под различные задачи.",
        isOpen: false
    },
    {
        icon: "icons/обучение7.svg",
        name: "Обучение и аттестация",
        description: "Проводим обучение для руководителей и линейного персонала.",
        isOpen: false
    },
    {
        icon: "icons/дашборд8.svg",
        name: "Отчётность / Dashboard",
        description: "Настроим и покажем как следить за ключевыми показателями.",
        isOpen: false
    },
    {
        icon: "icons/интеграция9.svg",
        name: "Интеграции сервисов с AmoCRM",
        description: "Интегрируем вашу CRM-систему с другими системами.",
        isOpen: false
    }, 
]);

function openDes(i) {
    data[i].isOpen = !data[i].isOpen;
}
</script>