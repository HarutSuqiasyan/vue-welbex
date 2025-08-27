<template>
    <header class="flex justify-center flex-wrap pt-15 max-md:gap-3 max-md:pt-5 max-[500px]:justify-evenly">
        <div class="order-1 cursor-pointer w-[140px] h-13 flex flex-col justify-between z-20 max-[500px]:order-1">
            <img class="w-[140px] h-6" src="/public/logo_welbex.svg" alt="logo">
            <p class="block text-light-text text-xs font-light w-[165px] h-6 max-lg:none">крупный интегратор AmoCRM в Росcии и ещё 8 странах</p>
        </div>
        <nav class="order-2 ml-[52px] mr-[140px] z-20 max-xl:mr-[50px] max-lg:mr-0 max-md:ml-0 items max-[500px]:order-3">
            <ul class="flex text-light-text cursor-pointer gap-[30px] font-medium text-15 flex-wrap max-md:justify-center max-md:items-center max-[520px]:gap-4 max-[520px]:text-[15px]">
                <li class="cursor-pointer hover:bg-gradient-to-r hover:from-orange-color hover:to-red-color hover:bg-clip-text hover:text-transparent font-inter">Услуги</li>
                <li class="cursor-pointer hover:bg-gradient-to-r hover:from-orange-color hover:to-red-color hover:bg-clip-text hover:text-transparent font-inter">Виджеты</li>
                <li class="cursor-pointer hover:bg-gradient-to-r hover:from-orange-color hover:to-red-color hover:bg-clip-text hover:text-transparent font-inter">Интеграции</li>
                <li class="cursor-pointer hover:bg-gradient-to-r hover:from-orange-color hover:to-red-color hover:bg-clip-text hover:text-transparent font-inter">Кейсы</li>
                <li class="cursor-pointer hover:bg-gradient-to-r hover:from-orange-color hover:to-red-color hover:bg-clip-text hover:text-transparent font-inter max-[705px]:hidden">Сертификаты</li>
            </ul>
        </nav>
        <div class="order-3 flex h-6 max-[500px]:order-2">
            <p class="text-light-text text-16 font-medium z-20 max-xl:ml-4 max-[500px]:hidden">+7 495 471-41-63</p>
            <div class="flex justify-center items-center pl-12 gap-7 z-20 max-xl:pl-3 max-xl:gap-3 ">
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
    </header>
</template>
<script setup>

</script>