<template>
    <div class="pt-40 pl-50 relative max-[1300px]:pl-15 max-sm:pl-3">
        <div class="absolute top-1/2 right-[-10%]  w-90 h-90 bg-orange-color rounded-full blur-2xl opacity-10 shadow-5xl " ></div>
        <div class="absolute top-[90%] right-[100px] w-12 h-12">
            <img src="/yellow_ball.svg" alt="">
        </div>
        <div>
            <h2 class="text-light-text text-5xl ">Мы решаем проблемы</h2>
        </div>
        <div class="flex gap-10 flex-wrap max-lg:gap-5 pt-15">
            <div class="flex gap-5">
                <p class="block text-2xl font-normal bg-gradient-to-r from-orange-color via-[24%] to-red-color bg-clip-text text-transparent">
                    99% компаний откладывают<br/> внедрение AmoCRM
                    <span class=" text-light-text">
                         или не доводят<br/> систему до результата
                    </span>
                </p>
            </div>
            <div>
                <p class="text-light-text font-light text-[18px]">Всё это приводит к самой главной<br/> проблеме — потере денег.</p>
            </div>
        </div>
        <div class="sm:hidden flex justify-center items-center pt-5 gap-3" >
            <div :class="current ? 'w-[140px] h-[70px] p-[2px]  bg-gradient-to-r from-[#FFD8A0] via-[#FD8787] to-[#DBA6FF] brightness-100':'w-[140px] h-[70px] p-[2px]  bg-gradient-to-r from-[#FFD8A0] via-[#FD8787] to-[#DBA6FF] brightness-10'" @click="current = true">
                <div class="w-full h-full bg-[#1a1d23]  flex items-center justify-center text-light-text text-center">
                    <p>Вы работаете<br/>без AmoCRM</p>
                </div>
            </div>
            <div :class="!current?'w-[140px] h-[70px] p-[2px]  bg-gradient-to-r from-[#FFD8A0] via-[#FD8787] to-[#DBA6FF] brightness-100':'w-[140px] h-[70px] p-[2px]  bg-gradient-to-r from-[#FFD8A0] via-[#FD8787] to-[#DBA6FF] brightness-10'" @click="current = false">
                <div class="w-full h-full bg-[#1a1d23]  flex items-center justify-center text-light-text text-center">
                    <p>AmoCRM не даёт<br/> результата</p>
                </div>
            </div>
        </div>
        <div v-if="current" class="flex flex-col items-center gap-5 flex-wrap pt-15 sm:hidden">
            <div>
                <div>
                    <h3 class="text-light-text text-[18px] font-medium">Компания работает без AmoCRM</h3>
                </div>
            </div>
            <div class="flex gap-2">
                <div class="line"></div>
                <p class="text-light-text text-[16px] font-light">Нет времени<br/>  на самостоятельное изучение<br/> и внедрение CRM системы.</p>
            </div>
            <div class="flex gap-2">
                <div class="line"></div>
                <p class="text-light-text text-[16px] font-light">Отсутствие понимания<br/> для чего надо внедрять CRM<br/> систему. Какую пользу это<br/> принесёт бизнесу.</p>
            </div>
            <div class="flex gap-2">
                <div class="line"></div>
                <p class="text-light-text text-[16px] font-light">Страх, что вложенные средства<br/> не окупятся.</p>
            </div>
        </div>
        <div v-else class="flex flex-col pt-15 items-center">
            <div>
                <h3 class="text-light-text text-[18px] font-medium">AmoCRM не даёт результата</h3>
            </div>
            <div class="flex flex-wrap">
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-5">
                <div class="flex gap-2">
                    <div class="line"></div>
                    <p class="text-light-text text-[16px] font-light">
                    Работа отдела продаж<br/> не является системной. Отдел<br/> является чёрным ящиком,<br/> работу которого нельзя<br/> спрогнозировать.
                    </p>
                </div>
                <div class="flex gap-2">
                    <div class="line"></div>
                    <p class="text-light-text text-[16px] font-light">
                    Информация о клиентах<br/> хранится лично у менеджеров,<br/> что тормозит проект,<br/> если сотрудник не на месте.<br/> Также это даёт возможность<br/> увести клиентов из компании.
                    </p>
                </div>
                <div class="flex gap-2">
                    <div class="line"></div>
                    <p class="text-light-text text-[16px] font-light">
                    Невозможно определить,<br/> какие сделки являются<br/> самыми прибыльными<br/> для компании, а какие<br/> не приносят результата.
                    </p>
                </div>
                <div class="flex gap-2">
                    <div class="line"></div>
                    <p class="text-light-text text-[16px] font-light">
                    Сложно оценить<br/> эффективность работы<br/> отдельного сотрудника.
                    </p>
                </div>
            </div>

            </div>
        </div>
        <div class="flex gap-48 flex-wrap max-[1050px]:gap-20 max-[920px]:gap-10 max-sm:hidden">
            <div class="flex flex-col gap-5 flex-wrap pt-15">
                <div>
                    <div>
                        <h3 class="text-light-text text-[18px] font-medium">Компания работает без AmoCRM</h3>
                    </div>
                </div>
                <div class="flex gap-2">
                    <div class="line"></div>
                    <p class="text-light-text text-[16px] font-light">Нет времени<br/>  на самостоятельное изучение<br/> и внедрение CRM системы.</p>
                </div>
                <div class="flex gap-2">
                    <div class="line"></div>
                    <p class="text-light-text text-[16px] font-light">Отсутствие понимания<br/> для чего надо внедрять CRM<br/> систему. Какую пользу это<br/> принесёт бизнесу.</p>
                </div>
                <div class="flex gap-2">
                    <div class="line"></div>
                    <p class="text-light-text text-[16px] font-light">Страх, что вложенные средства<br/> не окупятся.</p>
                </div>
            </div>
            <div class="flex flex-col pt-15 ">
                <div>
                    <h3 class="text-light-text text-[18px] font-medium">AmoCRM не даёт результата</h3>
                </div>
                <div class="flex flex-wrap">
                    <div class="grid grid-cols-2 grid-rows-2 gap-5">
                        <div class="flex gap-2">
                            <div class="line"></div>
                            <p class="text-light-text text-[16px] font-light">Работа отдела продаж<br/> не является системной. Отдел<br/> является чёрным ящиком,<br/> работу которого нельзя<br/> спрогнозировать.</p>
                        </div>
                        <div class="flex gap-2">
                            <div class="line"></div>
                            <p class="text-light-text text-[16px] font-light">Информация о клиентах<br/> хранится лично у менеджеров,<br/> что тормозит проект,<br/> если сотрудник не на месте.<br/> Также это даёт возможность<br/> увести клиентов из компании.</p>
                        </div>
                        <div class="flex gap-2">
                            <div class="line"></div>
                            <p class="text-light-text text-[16px] font-light">Невозможно определить,<br/> какие сделки являются<br/> самыми прибыльными<br/> для компании, а какие<br/> не приносят результата.</p>
                        </div>
                        <div class="flex gap-2">
                            <div class="line"></div>
                            <p class="text-light-text text-[16px] font-light">Сложно оценить<br/> эффективность работы<br/> отдельного сотрудника.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';
let current = ref(true)

</script>