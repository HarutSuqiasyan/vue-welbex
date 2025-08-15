<template>
    <div class="flex justify-center flex-wrap pt-15 ">
        <div class="cursor-pointer w-[140px] h-13 flex flex-col justify-between z-20 max-lg:hidden">
            <img class="w-[140px] h-6" src="/public/logo_welbex.svg" alt="logo">
            <p class="block text-light-text text-xs font-light w-[165px] h-6 max-lg:none">крупный интегратор AmoCRM в Росcии и ещё 8 странах</p>
        </div>
        <nav class="ml-[52px] mr-[140px] z-20 max-xl:mr-[50px] ">
            <ul class="flex text-light-text cursor-pointer gap-[30px] font-medium ">
                <li class="cursor-pointer hover:bg-gradient-to-r hover:from-orange-color hover:to-red-color hover:bg-clip-text hover:text-transparent font-inter text-15 max-lg:text-6">Услуги</li>
                <li class="cursor-pointer hover:bg-gradient-to-r hover:from-orange-color hover:to-red-color hover:bg-clip-text hover:text-transparent font-inter text-15 max-lg:text-6">Виджеты</li>
                <li class="cursor-pointer hover:bg-gradient-to-r hover:from-orange-color hover:to-red-color hover:bg-clip-text hover:text-transparent font-inter text-15 max-lg:text-6">Интеграции</li>
                <li class="cursor-pointer hover:bg-gradient-to-r hover:from-orange-color hover:to-red-color hover:bg-clip-text hover:text-transparent font-inter text-15 max-lg:text-6">Кейсы</li>
                <li class="cursor-pointer hover:bg-gradient-to-r hover:from-orange-color hover:to-red-color hover:bg-clip-text hover:text-transparent font-inter text-15 max-lg:text-6">Сертификаты</li>
            </ul>
        </nav>
        <div class="flex h-6 max-lg:hidden">
            <p class="text-light-text text-16 font-medium">+7 495 471-41-63</p>
            <div class="flex justify-center items-center pl-12 gap-7 max-xl:pl-3 max-xl:gap-3">
                <div>
                    <img class="w-6 h-6 max-xl:w-5 max-xl:h-5 hover:bg-blue-500 duration-200 rounded-2xl" src="/telegram.svg" alt="">
                </div>
                <div>
                    <img class="w-6 h-6 max-xl:w-5 max-xl:h-5 hover:bg-purple-500 duration-200 rounded-2xl" src="/viber.svg" alt="">
                </div>
                <div>
                    <img class="w-6 h-6 max-xl:w-5 max-xl:h-5 hover:bg-green-500 duration-200 rounded-2xl" src="/whatsapp.svg" alt="">
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>

</script>
