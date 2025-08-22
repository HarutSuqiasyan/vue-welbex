<template>
<div class="pl-50 pb-12 max-[1300px]:pl-15 max-[1024px]:pl-10 max-[768px]:pl-6 max-[480px]:pl-4 flex flex-col flex-wrap relative">
    <div class="absolute top-[20%] left-[20%] w-80 h-80 bg-[#833AB4] rounded-full blur-2xl opacity-10 shadow-2xl"></div>
    <div class="absolute top-[10%] left-[80%] w-80 h-80 bg-[#961A1A] rounded-full blur-2xl opacity-10 shadow-2xl"></div>
    <div class="absolute top-0 right-1/10 w-8 h-8">
        <img src="/red_ball.svg" alt="">
    </div>
    <div class="absolute bottom-0 left-1/3 w-8 h-8">
        <img src="/yellow_ball.svg" alt="">
    </div>
    <div class="py-12">
        <h3 class="text-5xl text-light-text max-md:text-3xl max-sm:text-2xl">Индивидуальный виджет</h3>
    </div>
    <div class="flex gap-45 pt-18 max-[1024px]:gap-20 max-[790px]:pt-12 max-[480px]:pt-6 max-[640px]:gap-8 flex-wrap">
        <div class="flex gap-5 flex-col">
            <p class="text-2xl bg-gradient-to-r from-orange-color via-[24%] to-red-color bg-clip-text text-transparent max-[640px]:text-xl max-[480px]:text-lg">Разработаем виджет<br/> индивидуально <span class="text-light-text">под ваши<br/> задачи</span></p>
            <p class="text-light-text text-[18px] font-light">Если вы не нашли<br/> подходящий из готовых<br/> вариантов.</p>
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
                Заказать аудит
                </button>
                <p v-if="isError" class="text-red-color text-[12px] font-extralight">Укажите номер телефона</p>
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

