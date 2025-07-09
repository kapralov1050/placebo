<template>
  <article class="w-2/3 grid grid-cols-[auto_1fr] grid-rows-2">
    <section
      class="flex flex-col justify-start items-start gap-y-10 px-10 py-5 mb-20"
    >
      <div class="flex justify-around mb-6 gap-x-4">
        <div
          v-for="location in locations"
          :key="location.id"
          class="flex flex-col justify-start items-start"
        >
          <h2 class="text-2xl">
            {{ location.city }}
          </h2>
          <p class="text-neutral-500 mb-4">
            {{ location.address }}
          </p>
          <p class="text-sm">
            {{ location.phone }}
          </p>
          <p class="text-sm">
            {{ location.email }}
          </p>
        </div>
      </div>
      <p class="text-xs text-neutral-500">
        Будни: 10:00—20:00
        <br />
        Выходные: 11:00—19:00
      </p>
    </section>
    <section
      class="w-full flex justify-between items-start p-3 before:content
        before:h-65 before:w-[1px] before:bg-neutral-500 before:mr-20"
    >
      <div class="flex flex-col gap-y-5">
        <div class="flex gap-x-3">
          <button
            class="border border-neutral-600 px-2 py-0.5 text-white rounded-lg
              flex justify-center items-center cursor-pointer"
          >
            Telegram
          </button>
          <button
            class="border border-neutral-600 px-2 py-0.5 text-white rounded-lg
              flex justify-center items-center cursor-pointer"
          >
            WhatsApp
          </button>
        </div>
        <p>Пишите круглосуточно. Ответим в рабочее время</p>
      </div>
      <div class="flex gap-x-1">
        <a href="#">
          <img
            src="/public/icon-vk.svg"
            alt="vk"
            class="bg-neutral-900 size-7 p-1.5 rounded-full"
          />
        </a>
        <a href="#">
          <img
            src="/public/icon-dzen.svg"
            alt="dzen"
            class="bg-neutral-900 size-6 p-1 rounded-full"
          />
        </a>
        <a href="#">
          <img
            src="/public/icon-instagram.svg"
            alt="instagram"
            class="bg-neutral-900 size-6 p-1 rounded-full"
          />
        </a>
        <a href="#">
          <img
            src="/public/icon-fb.svg"
            alt="fb"
            class="bg-neutral-900 size-6 p-1 rounded-full"
          />
        </a>
      </div>
    </section>
    <section
      class="flex flex-col col-span-2 before:content before:w-full
        before:h-[1px] before:bg-neutral-500"
    >
      <section class="flex items-start justify-between p-10 gap-x-10">
        <div class="flex gap-x-15">
          <p class="text-neutral-600 text-xs max-w-70">
            ООО «ЛОФТ ЭВЕНТ ХОЛЛ». Все права защищены. © 2015 — 2022
            <br />
            <br />
            «LOFT HALL» является зарегистрированным товарным знаком.
            <br />
            <br />
            Свидетельство № 777531 выдано Федеральной службой по
            интеллектуальной собственности 30.09.2020.
          </p>
          <p class="text-neutral-600 text-xs max-w-70">
            Юр. адрес: 115280, город Москва, ул. Ленинская Слобода, д. 26, пом.
            II-II, комн. 11
            <br />
            <br />
            ИНН/КПП: 7725360042 /772501001 ОГРН: 1177746215690
            <br />
            <br />
            Перепечатка и любое использование материалов возможно только при
            наличии ссылки на первоисточник.
          </p>
        </div>
        <div class="flex flex-col gap-y-5">
          <a href="#" class="inline-flex items-center gap-x-2">
            <img
              src="/public/logo-footer.png"
              alt="fb"
              class="size-8 p-1 rounded-full"
            />
            <span class="font-semibold text-xs text-neutral-500">
              Part of Placebo/25
            </span>
          </a>
          <div>
            <button
              class="w-full border border-neutral-600 px-2 py-1 text-xs
                text-neutral-500 rounded-lg flex justify-center items-center
                mb-3 cursor-pointer"
            >
              Мобильная версия
            </button>
            <button
              class="w-full border border-neutral-600 px-2 py-1 text-xs
                text-neutral-500 rounded-lg flex justify-center items-center
                cursor-pointer"
            >
              Скачать лого
            </button>
          </div>
        </div>
      </section>
    </section>
  </article>
</template>

<script setup>
  const locations = [
    {
      id: 1,
      city: 'Москва',
      address: 'Ленинская Слобода, 26с15',
      phone: '+7 (495) 120-19-05',
      email: 'info@lofthall.ru',
    },
    {
      id: 2,
      city: 'Подмосковье',
      address: 'Ленинская Слобода, 26с15',
      phone: '+7 (495) 120-19-05',
      email: 'info@lofthall.ru',
    },
    {
      id: 3,
      city: 'Санкт-Петербург',
      address: 'Арсенальная набережная, 1',
      phone: '+7 (812) 317-12-20',
      email: 'spb@lofthall.ru',
    },
  ]
</script>
