<template>
<div
    class="pl-50 max-[1300px]:pl-15 max-[1024px]:pl-10 max-[768px]:pl-6 max-[480px]:pl-4 flex flex-col flex-wrap relative">
    <div class="absolute top-40 left-[70%]">
        <img src="/purple_ball.svg" alt="">
    </div>
    <div class="absolute top-[320px] left-[-100px] w-70 h-70 bg-orange-color rounded-full blur-2xl opacity-10 shadow-2xl"></div>
    <div>
        <h3 class="text-5xl text-light-text max-md:text-3xl max-sm:text-2xl">
            Виджеты
        </h3>
    </div>
    <div
        class="flex flex-wrap gap-45 pt-18 max-[1024px]:gap-20 max-[790px]:pt-12 max-[480px]:pt-6 max-[640px]:gap-8 " >
        <p
            class="text-light-text text-2xl font-medium max-[640px]:text-xl max-[480px]:text-lg"
            >
            Для вас разработали<br />
            <span
                class="text-2xl bg-gradient-to-r from-orange-color via-[24%] to-red-color bg-clip-text text-transparent max-[640px]:text-xl max-[480px]:text-lg"
                >
            готовые решения<br />
            в виде виджетов
            </span>
        </p>
        <p
            class="text-light-text text-[18px] font-light max-[640px]:text-base max-[480px]:text-sm"
            >
            20 виджетов помогут<br />
            автоматизировать ваш отдел.
        </p>
    </div>
    <div class="border-1 border-[#25262c] flex flex-wrap gap-3 max-lg:justify-center">
        <div class="w-[60%] pt-15 max-[1024px]:w-[85%] max-[768px]:w-full">
            <h3 class="text-[18px] text-light-text">Основные возможности:</h3>
            <div
                class="text-light-text text-[16px] font-light grid grid-cols-2 gap-2 pt-8 w-[60%] pb-40 max-[1024px]:w-[80%] max-[768px]:w-full max-[640px]:grid-cols-1 max-sm:pb-20"
                >
                <div class="flex gap-3">
                    <div class="line"></div>
                    <p>Загрузка файлов любого<br />формата</p>
                </div>
                <div class="flex gap-3">
                    <div class="line"></div>
                    <p>
                        Отображение файлов прямо<br />
                        в сделке в виде примечания,<br />
                        а так же в панели справа
                    </p>
                </div>
                <div class="flex gap-3">
                    <div class="line"></div>
                    <p>
                        Сортировка всех файлов<br />
                        по папкам
                    </p>
                </div>
            </div>
            <div class="text-light-text flex flex-col gap-3">
                <div
                    class="flex items-end gap-15 flex-wrap max-[600px]:gap-6 max-[480px]:items-start"
                    >
                    <div class="flex flex-col gap-3">
                        <h3 class="text-[18px]">
                            Попробуйте виджет Яндекс Диск<br />
                            бесплатно:
                        </h3>
                        <div class="flex gap-3">
                            <div class="line"></div>
                            <p class="text-[16px] font-light">1 месяц бесплатно</p>
                        </div>
                        <div class="flex gap-3">
                            <div class="line"></div>
                            <p class="text-[16px] font-light">
                                Затем выберите тариф <br />
                                на 6, 9, 12 или 24 месяца
                            </p>
                        </div>
                    </div>
                    <div
                        class="button_active w-66 h-15 max-[640px]:w-full max-[640px]:h-auto max-[640px]:text-center"
                        >
                        Попробовать бесплатно
                    </div>
                </div>
            </div>
        </div>
        <div class="flex flex-col ">
            <div 
            v-for="(item, i) in data" 
            :key="i" 
            class="flex items-center text-light-text opacity-30 bg-black w-90 h-20 cursor-pointer" 
            @click="toggleItem(item.id)" 
            :class="{ 'opacity-100': item.isOpen }">
                <img :src="item.img" alt="" class="px-3">
                <p>{{ item.title }}</p>
            </div>


        </div>
    </div>
</div>
</template>

<script setup>
import { ref } from 'vue'

let data = ref([
  {
    id: 0,
    title: 'Яндекс Диск',
    img: '/Section9/Rectangle1.svg',
    isOpen: false,
  },
  {
    id: 1,
    title: 'Google Drive',
    img: '/Section9/logos2.svg',
    isOpen: false,
  },
  {
    id: 2,
    title: 'Распределение заявок',
    img: '/Section9/people3.svg',
    isOpen: false,
  },
  {
    id: 3,
    title: 'Время на этапе',
    img: '/Section9/clock4.svg',
    isOpen: false,
  },
  {
    id: 4,
    title: 'История посещений',
    img: '/Section9/history5.svg',
    isOpen: false,
  },
  {
    id: 5,
    title: 'Синхронизация сделок',
    img: '/Section9/synchronization6.svg',
    isOpen: false,
  },
  {
    id: 6,
    title: 'Синхронизация с Asana',
    img: '/Section9/image7.svg',
    isOpen: false,
  },
  {
    id: 7,
    title: 'Уведомление в Telegram',
    img: '/Section9/bx_bxl-telegram8.svg',
    isOpen: false,
  },
])

function toggleItem(id) {
  data.value = data.value.map(item => {
    if (item.id === id) {
      item.isOpen = !item.isOpen
    }
    return item
  })
}
</script>
