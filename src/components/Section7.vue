<template>
    <div class="fixed inset-0 bg-black/50 backdrop-blur-sm z-40 hidden"></div>
    <div :class="modalVisible?'fixed left-1/2 top-1/2 w-1/2 h-65 -translate-x-1/2 -translate-y-1/2 z-50 bg-black':'hidden'">
        <div :class="modalVisible?'relative flex flex-col justify-center text-center h-full gap-2':'hidden'">
            <div class="absolute right-2 top-2 cursor-pointer" @click="closeModal">
                <img src="/close.svg" alt="">
            </div>
            <p class="font-normal text-2xl bg-gradient-to-r from-orange-color via-[24%] to-red-color bg-clip-text text-transparent">Спасибо за вашу заявку!</p>
            <p class="text-light-text text-[16px]">Наш менеджер свяжется с вами в ближайшее время и уточнит все детали.</p>
        </div>
    </div>


  <div class="relative pt-25 pl-50 max-[1300px]:pl-15 max-md:pl-5 max-sm:pt-10">
    <div>
        <img class="absolute top-[41%] left-[30%]" src="/purple_ball.svg" alt="">
    </div>
    <div>
        <img class="absolute top-[75%] left-50" src="/yellow_ball.svg" alt="">
    </div>
    <div>
        <img class="absolute top-[80%] left-1/3 w-7 h-7" src="/red_ball.svg" alt="">
    </div>
    <div>
        <img class="absolute top-[95%] right-1/10" src="/red_ball.svg" alt="">
    </div>
    <div class="flex max-lg:flex-col z-40">
      <div class="relative h-[700px] max-lg:h-auto">
        <div>
          <h3 class="text-5xl text-light-text max-md:text-3xl max-sm:text-2xl">
            Расчёт стоимости
          </h3>
        </div>
        <div class="flex flex-col gap-5 pt-15 max-md:pt-8">
          <p class="text-light-text text-2xl font-light max-md:text-xl max-sm:text-base">
            Ответьте на 4 вопроса<br />
            и получите
            <span
              class="font-normal bg-gradient-to-r from-orange-color via-[24%] to-red-color bg-clip-text text-transparent"
              >расчёт стоимости<br />внедрения AmoCRM</span
            >
          </p>
          <p class="text-light-text text-[18px] font-light max-md:text-base max-sm:text-sm">
            И сэкономьте 80% своего<br />времени.
          </p>
        </div>
        <div class="absolute top-[45%] left-[-17%] max-lg:hidden lg:left-[-17%] md:left-[-5%] sm:left-[0] 
                    lg:top-[45%] md:top-[50%] sm:top-[55%] z-30">
            <img src="/Polyhedron.svg" alt="" class="w-[clamp(200px,25vw,400px)] h-auto bg-[url(/dots.svg)]" />
        </div>
        <div class="lg:hidden mt-10 flex justify-center">
            <img src="/Polyhedron.svg" alt="" class="w-[clamp(180px,50vw,350px)] h-auto bg-[url(/dots.svg)]" />
        </div>
        </div>

      <div class="flex flex-col pt-27 gap-5 max-md:pt-10">
        <div>
          <p class="text-[18px] text-light-text font-light max-md:text-base max-sm:text-sm">
            При заказе с сайта вы получите<br />4 бонуса от компании:
          </p>
          <div class="grid grid-cols-2 gap-5 pt-5 max-sm:grid-cols-1 max-sm:gap-3">
            <div class="flex">
              <div class="line m-2"></div>
              <p class="text-light-text text-sm font-light">
                Аудит с лучшим экспертом компании
              </p>
            </div>
            <div class="flex">
              <div class="line m-2"></div>
              <p class="text-light-text text-sm font-light">30 виджетов</p>
            </div>
            <div class="flex">
              <div class="line m-2"></div>
              <p class="text-light-text text-sm font-light">
                Dashboard с показателями
              </p>
            </div>
            <div class="flex">
              <div class="line m-2"></div>
              <p class="text-light-text text-sm font-light">35 дней AmoCRM</p>
            </div>
          </div>

          <div class="pt-10">
            <div>
              <p class="question pt-5">1. Пользуетесь amoCRM?</p>
              <div class="flex gap-2 pt-4 flex-wrap max-sm:flex-col max-sm:gap-2">
                <div @click="toggleButton(0)" :class="button1?'button_active':'button_inactive'">Нет, планирую</div>
                <div @click="toggleButton(1)" :class="button2?'button_active':'button_inactive'">Да, меньше года</div>
                <div @click="toggleButton(2)" :class="button3?'button_active':'button_inactive'">Да, 1-3 года</div>
                <div @click="toggleButton(3)" :class="button4?'button_active':'button_inactive'">Да, более 3-х лет</div>
              </div>
            </div>

            <div>
              <p class="question pt-5">2. Сколько менеджеров у вас в штате?</p>
              <div class="flex gap-2 pt-4 flex-wrap max-sm:flex-col max-sm:gap-2">
                <div @click="toggleButton2(0)" :class="button5?'button_active':'button_inactive'">1-3</div>
                <div @click="toggleButton2(1)" :class="button6?'button_active':'button_inactive'">4-10</div>
                <div @click="toggleButton2(2)" :class="button7?'button_active':'button_inactive'">11-20</div>
                <div @click="toggleButton2(3)" :class="button8?'button_active':'button_inactive'">Более 20</div>
              </div>
            </div>

            <div>
              <p class="question pt-5">3. Пользуетесь виджетами?</p>
              <div class="flex gap-2 pt-4 flex-wrap max-sm:flex-col max-sm:gap-2">
                <div @click="toggleButton3(0)" :class="button9?'button_active':'button_inactive'">Нет</div>
                <div @click="toggleButton3(1)" :class="button10?'button_active':'button_inactive'">Да, 1-3 виджета</div>
                <div @click="toggleButton3(2)" :class="button11?'button_active':'button_inactive'">Да, 4-8 виджетов</div>
                <div @click="toggleButton3(3)" :class="button12?'button_active':'button_inactive'">Да, более 8 виджетов</div>
              </div>
            </div>

            <div>
              <p class="question pt-5">4. Выберите бонус, который хотите получить</p>
              <div class="flex gap-2 pt-4 flex-wrap max-sm:flex-col max-sm:gap-2">
                <div @click="toggleButton4(0)" :class="button13?'button_active':'button_inactive'">
                  <img src="/bxs-widget.svg.svg" alt="" />
                  30 виджетов
                </div>
                <div @click="toggleButton4(1)" :class="button14?'button_active ':'button_inactive'">
                  <img src="/bxs-discount.svg.svg" alt="" />
                  20% на доработку AmoCRM
                </div>
              </div>
            </div>

            <div class="flex-1 flex items-end gap-8 flex-wrap min-w-[250px] pt-10 max-sm:flex-col max-sm:items-start">
              <div class="flex flex-col gap-7 max-[685px]:gap-3 w-full">
                <div class="flex flex-col gap-2 w-full">
                  <div>
                    <p class="text-[#656566] text-[18px] font-montserrat font-light max-sm:text-sm">Ваш номер телефона</p>
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
                      class="max-sm:w-full"
                    />
                  </div>
                </div>

                <div class="w-full">
                  <button @click="checkTel" class="text-white w-[262px] max-w-full h-[62px] bg-blue-color font-montserrat text-[16px] flex justify-center items-center max-sm:w-full">
                    Заказать аудит
                  </button>
                  <p v-if="isError" class="text-red-color text-[12px] font-extralight">Укажите номер телефона</p>
                </div>
              </div>

              <div>
                <p class="text-light-text text-[12px] font-extralight max-sm:text-[10px]">
                  Нажимая «Заказать аудит», я даю согласие<br />
                  на <span class="underline">обработку персональных данных</span>
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, reactive } from "vue";
let button1 = ref(true)
let button2 = ref(false)
let button3 = ref(false)
let button4 = ref(false)
let button5 = ref(true)
let button6 = ref(false)
let button7 = ref(false)
let button8 = ref(false)
let button9 = ref(true)
let button10 = ref(false)
let button11 = ref(false)
let button12 = ref(false)
let button13 = ref(true)
let button14 = ref(false)
let buttons = reactive([button1, button2, button3, button4]);
function toggleButton(index) {
    buttons.forEach((button, i) => {
        if (i === index) {
            button.value = true;
        } else {
            button.value = false;
        }
    });
}
let buttons2 = reactive([button5, button6, button7, button8]);
function toggleButton2(index) {
    buttons2.forEach((button, i) => {
        if (i === index) {
            button.value = true;
        } else {
            button.value = false;
        }
    });
}
let buttons3 = reactive([button9, button10, button11, button12]);
function toggleButton3(index) {
    buttons3.forEach((button, i) => {
        if (i === index) {
            button.value = true;
        } else {
            button.value = false;
        }
    });
}
let buttons4 = reactive([button13, button14]);
function toggleButton4(index) {
    buttons4.forEach((button, i) => {
        if (i === index) {
            button.value = true;
        } else {
            button.value = false;
        }
    });
}
const modalVisible = ref(false);
function openModal() {
    modalVisible.value = true;
}
function closeModal() {
    modalVisible.value = false;
}
const phone = ref("");

const isError = ref(false)
function checkTel(){
    if(phone.value.length !== 16){
        isError.value = true
    }else{
        openModal()
        phone.value = ""
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