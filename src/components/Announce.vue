<template>
  <aside class="w-2/3 px-8 flex flex-col items-center relative mt-40">
    <div
      class="container flex justify-between bg-indigo-900 p-7 rounded-xl z-10"
    >
      <div class="">
        <h2 class="font-medium text-2xl">Новогодний корпоратив</h2>
        <p class="text-white/70">
          Стильные залы с декором и крафтовой мебелью. Качественный звук,
          авторская кухня, нет «пробки».
        </p>
      </div>
      <a
        :href="$props.link"
        target="_blank"
        rel="noopener"
        class="self-end relative z-10 cursor-pointer"
      >
        Подробнее →
      </a>
    </div>
    <div class="w-[93%] h-27 bg-indigo-950 absolute z-4 rounded-3xl top-3" />
  </aside>
</template>

<script setup></script>
