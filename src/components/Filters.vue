<template>
  <div class="w-2/3 flex flex-col justify-start items-start px-10 mb-10">
    <h2 class="text-2xl mb-2">Залы в Москве</h2>
    <section class="container">
      <ul class="flex gap-x-1 mb-2">
        <li v-for="qty in qtyFilters">
          <button
            class="border border-neutral-600 px-6 py-1 text-neutral-200
              rounded-4xl cursor-pointer"
          >
            {{ qty.label }}
          </button>
        </li>
      </ul>
      <ul class="flex gap-x-1">
        <li v-for="event in eventsFilters">
          <button
            class="border border-neutral-600 px-6 py-1 text-neutral-200
              rounded-4xl cursor-pointer"
          >
            {{ event.label }}
          </button>
        </li>
      </ul>
    </section>
    <section>
      <div></div>
    </section>
  </div>
</template>

<script setup lang="ts">
  const qtyFilters = [
    { id: 1, label: 'До 100 персон' },
    { id: 2, label: 'До 500 персон' },
    { id: 3, label: 'Больше 500 персон' },
  ]

  const eventsFilters = [
    { id: 1, label: 'Для стильной свадьбы' },
    { id: 2, label: 'Масштабная конференция' },
  ]
</script>

<style scoped lang="scss"></style>
