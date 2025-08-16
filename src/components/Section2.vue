<template>
    <div class="flex relative flex-col lg:flex-row justify-center max-[1110px]:pt-20 max-lg:pt-10">
        <div class="absolute bottom-[-200px] left-[75%] w-70 h-70 bg-red-color rounded-full blur-2xl opacity-5 shadow-2xl z-30 " ></div>
        <div class="absolute bottom-[35%] right-[30%] z-30 w-10 h-10">
            <img src="/purple_ball.svg" alt="">
        </div>
    <div class="flex flex-col w-full  lg:w-1/2 px-5 lg:pl-20 h-auto lg:h-[500px] lg:justify-between gap-y-8">
      <div>
        <h2 class="text-light-text font-inter font-medium text-5xl max-lg:text-4xl text-center lg:text-left">
          Давайте знакомиться
        </h2>
      </div>

      <div class="flex justify-center lg:justify-start">
        <p
          class="bg-gradient-to-r from-orange-color to-red-color bg-clip-text text-transparent font-inter text-2xl font-normal text-center lg:text-left"
        >
          Посмотрите минутное видео<br />
          <span class="text-light-text font-extralight">от основателя компании</span>
        </p>
      </div>

      <div class="flex flex-col items-center lg:flex-row lg:items-end gap-5 z-20 justify-center lg:justify-start text-center">
        <img
          class="w-[200px] max-w-[80%] brightness-50 hover:brightness-100 mx-auto lg:w-115 lg:h-65"
          src="/Rectangle.svg"
          alt="preview"
        />
        <div class="flex flex-col gap-3">
          <div
            class="flex justify-center items-center w-[55px] h-[55px] rounded-full bg-transparent border-light-text border-2 border-solid hover:bg-blue-color hover:border-none hover:shadow-2xl max-lg:hidden"
          >
            <img src="/Vector.svg" alt="play button" />
          </div>
          <p
            class="text-sm font-montserrat font-light text-light-text w-[170px] max-lg:hidden"
          >
            Посмотрите видео<br />и получите подарок
          </p>
        </div>
      </div>
    </div>

    <div class="relative h-[500px] w-full lg:w-1/2 max-lg:hidden">
      <div class="absolute inset-0 bg-[linear-gradient(to_bottom_right,rgba(14,16,20,0.8)_50%,rgba(186,86,209,0.8)_100%)]"></div>
      <p
        class="text-light-text text-sm font-light absolute top-[200px] left-[200px] max-[1307px]:left-[140px]"
      >
        Михаил Доброхвалов<br />— основатель WelbeX.
      </p>
      <img
        class="absolute bottom-[-10px] right-0"
        src="/фото_михаила.svg"
        alt="Михаил Доброхвалов"
      />
    </div>
  </div>
</template>

<script setup>
</script>
