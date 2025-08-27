<template>
    <div class="pl-50 py-25 max-[1300px]:pl-15 max-[1024px]:pl-10 max-[768px]:pl-6 max-[480px]:pl-4 flex flex-col flex-wrap relative">
        <div class="pb-15">
            <h3 class="text-5xl text-light-text max-md:text-3xl max-sm:text-2xl">Бесплатный доступ к системе</h3>
        </div>
        <div class="flex gap-30 max-md:gap-15 max-[536px]:flex-wrap">
            <div>
                <div class="flex flex-col gap-5 flex-wrap max-[712px]:gap-20 relative z-20">
                    <p class="text-light-text font-medium text-2xl max-[640px]:text-xl max-[480px]:text-lg">Получите доступ к полному<br/> функционалу<span class="text-2xl bg-gradient-to-r from-orange-color via-[24%] to-red-color bg-clip-text text-transparent"> AmoCRM<br/> на 35 дней</span></p>
                    <div class="flex flex-col gap-2">
                        <p class="text-light-text text-[16px] font-light max-[640px]:text-base max-[480px]:text-sm">Наш сотрудник ответит<br/> на все возникшие вопросы<br/> и проконсультирует<br/> по функционалу AmoCRM..</p>
                        <p class="text-light-text text-[16px] font-light max-[640px]:text-base max-[480px]:text-sm">Попробуйте уже сегодня<br/> и вы поймёте насколько<br/> это удобно и просто! </p>
                    </div>
                </div>
            </div>
            <div class="flex flex-col gap-7">
                <div>
                    <h3 class="text-light-text">Вместе с доступом<br/> к системе вы получите:</h3>
                </div>
                <div class="text-light-text">
                    <div class="flex gap-2">
                        <div class="line"></div>
                        <p>Аудит с лучшим экспертом компании</p>
                    </div>
                    <div class="flex gap-2">
                        <div class="line"></div>
                        <p>Dashboard с показателями</p>
                    </div>
                    <div class="flex gap-2">
                        <div class="line"></div>
                        <p>30 виджетов</p>
                    </div>
                </div>
                <div class="flex flex-col gap-7 max-[685px]:gap-3">
                    <div class="flex flex-col gap-2">
                        <div>
                            <p class="text-[#656566] text-[18px] font-montserrat font-light">Ваш номер телефона</p>
                        </div>
                        <div>
                            <input
                                v-model="phone"
                                type="tel"
                                placeholder="+7(___)___-__-__"
                                :class="isError === false
                                ? 'bg-[#000] w-[262px] max-w-full h-[62px] text-light-text border-2 border-[#656566] placeholder-light-text'
                                : 'bg-[#000] w-[262px] max-w-full h-[62px] text-light-text border-2 border-red-color placeholder-light-text'"
                                @input="formatPhone"
                                />
                        </div>
                    </div>
                    <div>
                        <button @click="checkTel" class="text-white w-[262px] max-w-full h-[62px] bg-blue-color font-montserrat text-[16px] flex justify-center items-center">
                        Получить доступ
                        </button>
                        <p v-if="isError" class="text-red-color text-[12px] font-extralight">Укажите номер телефона</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
    import { ref } from "vue";

    const phone = ref("");

    const isError = ref(false)
    function checkTel(){
        if(phone.value.length !== 16){
            isError.value = true
        }else{
            isError.value = false
        }
    }
    function formatPhone(e) {
    let value = e.target.value.replace(/\D/g, ""); 
    if (value.startsWith("7")) {
        value = value.slice(1); 
    }

    let formatted = "+7";
    if (value.length > 0) formatted += "(" + value.substring(0, 3);
    if (value.length >= 3) formatted += ")" + value.substring(3, 6);
    if (value.length >= 6) formatted += "-" + value.substring(6, 8);
    if (value.length >= 8) formatted += "-" + value.substring(8, 10);

    phone.value = formatted;
    }
</script>