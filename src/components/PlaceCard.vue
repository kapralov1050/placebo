<template>
  <section class="w-100 h-125 flex flex-col items-start">
    <a class="cursor-pointer">
      <img
        :src="place.image"
        :alt="place.name"
        class="w-100 h-auto mb-5 transition-all duration-300 hover:scale-102"
      />
    </a>
    <div class="px-5">
      <h2 class="text-2xl mb-3">
        {{ place.name }}
      </h2>
      <ul class="flex gap-x-1 text-[0.9rem] mb-4">
        <li
          class="bg-neutral-800 px-1.5 py-0.7 text-white rounded-lg flex
            justify-center items-center"
        >
          {{ place.area }} м²
        </li>
        <li
          class="bg-neutral-800 px-1.5 py-0.7 text-white rounded-lg flex
            justify-center items-center"
        >
          {{ place.capacity[0] }} - {{ place.capacity[1] }} персон
        </li>
        <li
          class="bg-neutral-800 px-1.5 py-0.7 text-white rounded-lg flex
            justify-center items-center"
        >
          {{ place.location }}
        </li>
      </ul>
      <p class="text-[0.9rem] text-neutral-200 leading-relaxed">
        {{ place.description }}
      </p>
    </div>
  </section>
</template>

<script setup>
  const props = defineProps({
    place: {
      id: Number,
      name: String,
      image: String,
      area: Number,
      capacity: Array,
      location: String,
      description: String,
    },
  })
</script>

<style scoped lang="scss"></style>
