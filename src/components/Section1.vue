<template>
    <div class="flex justify-center flex-wrap min-h-screen   ">
        <div class="order-1 flex flex-col gap-7 pt-25 z-20 pl-10 max-[550px]:gap-3 max-[550px]:pl-0 max[550px]:pb-10 max-[550px]:text-center">
            <h2 class="text-light-text leading-15 text-5xl font-medium font-inter max-[380px]:text-4xl">Зарабатывайте<br/>больше</h2>
            <p class="text-5xl font-bold bg-gradient-to-r from-[#FCB045] via-[#FCB045] via-[24%] to-[#FF3F78] bg-clip-text text-transparent ">с AmoCRM.</p>
            <p class="text-light-text text-14.5 font-medium font-montserrat">Развиваем и контролируем<br/> продажи за вас</p>
        </div>
        <div class=" order-2 flex w-[540px] h-[551px] justify-center items-center z-10 max-xl:w-[400px] max-xl:h-[410px] max-lg:w-[300px] max-lg:h-[300px] max-md:order-3 animate-spin [animation-duration:5s]">
            <img class="bg-[url(/dots.svg)]" src="/Polyhedron.svg" alt="">
        </div>
        <div class="order-3 flex flex-col items-center z-20 justify-center gap-10 max-md:order-2 max-lg:gap-5 max-md:justify-end max-[1340px]:mr-15 max-md:mr-0">
            <p class="text-light-text font-inter text-18 text-end z-20 max-sm:pt-2.5 max-[550px]:text-start">Вместе с <span class="bg-gradient-to-r from-orange-color to-red-color bg-clip-text text-transparent font-inter font-black ">БЕСПЛАТНОЙ<br/> КОНСУЛЬТАЦИЕЙ</span> мы дарим:</p>
            <div class="text-light-text grid grid-cols-2 grid-rows-2 gap-[30px] grid-flow-col z-20">
                <div class="flex flex-col justify-center items-center">
                    <h2 class="uppercase text-18 font-medium max-md max-lg:font-extralight"><span class=" bg-gradient-to-r from-orange-color to-red-color bg-clip-text text-transparent">- </span>Виджеты</h2>
                    <p class="font-montserrat text-end text-16 font-light max-md:hidden max-lg:text-13 ">30 готовых<br/> решений</p>
                </div>
                <div class="flex flex-col justify-center items-center">
                    <h2 class=" uppercase text-18 font-medium max-md max-lg:font-extralight"><span class=" bg-gradient-to-r from-orange-color to-red-color bg-clip-text text-transparent">- </span>Dashboard</h2>
                    <p class="font-montserrat text-end text-16 font-light max-md:hidden max-lg:text-13">с показателями<br/> вашего бизнеса</p>
                </div>
                <div class="flex flex-col justify-center items-center">
                    <h2 class=" uppercase text-18 font-medium max-md max-lg:font-extralight"><span class=" bg-gradient-to-r from-orange-color to-red-color bg-clip-text text-transparent">- </span>Skype Аудит</h2>
                    <p class="font-montserrat text-end text-16 font-light max-md:hidden max-lg:text-13">отдела продаж<br/> и CRM системы</p>
                </div>
                <div class="flex flex-col justify-center items-center">
                    <h2 class=" uppercase text-18 font-medium max-md max-lg:font-extralight"><span class=" bg-gradient-to-r from-orange-color to-red-color bg-clip-text text-transparent">- </span>35 дней</h2>
                    <p class="font-montserrat text-end text-16 font-light max-md:hidden max-lg:text-13">использования<br/> AmoCRM</p>
                </div>
            </div>
            <div>
                <button class="w-[262px] h-[61px] text-light-text bg-blue-color text-16 font-medium hover:drop-shadow-lg/30 shadow-blue-color cursor-pointer max-lg:w-[162px] max-lg:h-9 max-lg:text-sm 
                max-[548px]:hidden">Получить консультацию</button>
            </div>
        </div>
        <div class="w-full z-20 h-[54px] hidden absolute top-190 max-[548px]:block text-sm font-inter font-medium text-light-text">
            <button class="w-[60%] h-full bg-blue-color ">Получить консультацию</button>
            <button class="w-[40%] h-full bg-[#396ADB]">Позвонить нам</button>
        </div>
    </div>
</template>
<script setup>

</script>