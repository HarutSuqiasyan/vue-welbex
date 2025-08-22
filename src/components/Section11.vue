<template>
  <div class="pt-30 pl-50 max-[1300px]:pl-15 max-[1024px]:pl-10 max-[768px]:pl-6 max-[480px]:pl-4">
    <div>
      <div>
        <div class="text-5xl text-light-text max-md:text-3xl max-sm:text-2xl">
          Интеграции
        </div>
        <div>
          <p
            class="text-light-text text-2xl font-normal max-[640px]:text-xl max-[480px]:text-lg py-15"
          >
            Интегрируем и дорабатываем<br />
            практически
            <span
              class="text-2xl bg-gradient-to-r from-orange-color via-[24%] to-red-color bg-clip-text text-transparent max-[640px]:text-xl max-[480px]:text-lg"
              >любой<br />
              сервис</span
            >
            в AmoCRM
          </p>
        </div>
      </div>

      <div class="flex flex-col gap-10">
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
          <div
            v-for="(item, index) in data"
            :key="index"
            class="flex flex-col items-start gap-3"
          >
            <p class="text-lg font-medium text-light-text text-[18px]">
              {{ item.title.toUpperCase() }}
            </p>
            <div class="flex flex-col items-start gap-3">
              <img
                v-for="(img, i) in [item.img1, item.img2, item.img3]"
                :key="i"
                :src="img"
                alt="logo"
                class="h-8 object-contain"
              />
            </div>
          </div>
        </div>

        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
          <div
            v-for="(item, index) in data2"
            :key="index"
            class="flex flex-col items-start justify-center gap-3"
          >
            <p class="text-[16px] font-medium text-light-text">
              {{ item.title.toUpperCase() }}
            </p>
            <img :src="item.img" alt="logo" class="h-8 object-contain" />
          </div>
        </div>

        
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
          <div
            v-for="(item, index) in data3"
            :key="index"
            class="flex flex-col items-start gap-3"
          >
            <p class="text-lg font-medium text-light-text text-[18px]">
              {{ item.title.toUpperCase() }}
            </p>
            <div class="flex flex-col items-start gap-3">
              <img
                v-for="(img, i) in [item.img1, item.img2]"
                :key="i"
                :src="img"
                alt="logo"
                class="h-8 object-contain"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<script setup>
import { ref } from "vue";

let data = ref([
  {
    title: "Социальные сети",
    img1: "/Section11/3Logo/Facebook1.svg",
    img2: "/Section11/3Logo/Frame23.svg",
    img3: "/Section11/3Logo/instagram4.svg",
  },
  {
    title: "E-mail маркетинг",
    img1: "/Section11/3Logo/mc5.svg",
    img2: "/Section11/3Logo/sendpulse6.svg",
    img3: "/Section11/3Logo/image7.svg",
  },
  {
    title: "Мессенджеры",
    img1: "/Section11/3Logo/image8.svg",
    img2: "/Section11/3Logo/pact9.svg",
    img3: "/Section11/3Logo/Main10.svg",
  },
  {
    title: "Телефония",
    img1: "/Section11/3Logo/global11.svg",
    img2: "/Section11/3Logo/image12.svg",
    img3: "/Section11/3Logo/mango13.svg",
  },
]);
let data2 = ref([
    {
        title: 'Голосовые прозвоны',
        img: '/Section11/1Logo/toggle-logo-1.svg',
    },
    {
        title: 'Складские сервисы',
        img: '/Section11/1Logo/header-logo-2.svg'
    },
    {
        title: 'Бизнес аналитика',
        img: '/Section11/1Logo/PowerBI-logo-3.svg'
    },
    {
        title: 'Бухгалтерия',
        img: '/Section11/1Logo/logo4.svg'
    }
])
let data3 = ref([
    {
        title: 'Онлайн-банкинг',
        img1: '/Section11/2Logo/Vector1.svg',
        img2: '/Section11/2Logo/logo_yandex2.svg'
    },
    {
        title: 'SMS рассылки',
        img1: '/Section11/2Logo/smsc_logo3.svg',
        img2: '/Section11/2Logo/logo-top4.svg'
    },
    {
        title: 'Сервисы',
        img1: '/Section11/2Logo/logos_yandex5.svg',
        img2: '/Section11/2Logo/grommet6.svg'
    }
])
</script>
