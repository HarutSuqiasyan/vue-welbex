<template>
  <div class="relative pl-50 pt-36 max-[1300px]:pl-15 max-[1024px]:pl-10 max-[768px]:pl-6 max-[480px]:pl-4">
    <div class="absolute right-1/5 w-20 h-20"><img src="/red_ball.svg" alt=""></div>
    <div class="absolute w-10 h-10 top-[95%] right-1/25"><img src="/purple_ball.svg" alt=""></div>

    <div class="pb-18">
      <h3 class="text-light-text text-5xl font-normal">Бесплатный аудит</h3>
    </div>
    <div class="pt-12 flex flex-wrap gap-35 max-[1024px]:gap-10 max-[768px]:gap-6">
      <div class="flex-1 min-w-[250px]">
        <div class="flex flex-col gap-5">
          <p class="text-light-text text-2xl">
            Закажите<br/>
            <span class="font-normal bg-gradient-to-r from-orange-color via-[24%] to-red-color bg-clip-text text-transparent">
              бесплатный скайп-аудит<br/> отдела продаж
            </span>
          </p>
          <p class="text-light-text font-light text-[18px]">И получите предложение<br/> по решению вашей задачи</p>
        </div>
      </div>

      <div class="flex-1 flex items-end gap-8 flex-wrap min-w-[250px]">
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

        <div>
          <p class="text-light-text text-[12px] font-extralight">Нажимая «Заказать аудит», я даю согласие<br/> на <span class="underline">обработку персональных данных</span></p>
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