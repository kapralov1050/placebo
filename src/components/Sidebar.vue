<template>
  <aside class="fixed h-full flex flex-col justify-start pt-13 pl-10 z-10">
    <img src="../assets/sidebar-logo.svg" class="mb-6 size-15" ref="logo" />
    <nav class="text-xs">
      <ul class="flex flex-col gap-y-1 mb-4 relative" ref="locations">
        <li v-for="city in cities" :key="city.name">
          <a
            href="#"
            :class="{
              'text-neutral-600': !city.isActive,
              'before:content before:rounded-full before:size-2 before:bg-white before:absolute before:-left-4 before:top-2':
                city.isActive,
            }"
            class="hover:text-neutral-300 transition-colors"
          >
            {{ city.name }}
          </a>
        </li>
      </ul>
      <ul class="flex flex-col gap-y-1 relative" ref="menu">
        <li v-for="item in menuItems" :key="item.name">
          <a
            href="#"
            class="text-neutral-100 hover:text-neutral-300 transition-colors"
          >
            {{ item.name }}
          </a>
        </li>
      </ul>
    </nav>
  </aside>
</template>

<script setup lang="ts">
  import { ref, onMounted } from 'vue'
  import gsap from 'gsap'
  import { SplitText } from 'gsap/SplitText'

  gsap.registerPlugin(SplitText)

  const logo = ref(null)
  const locations = ref(null)
  const menu = ref(null)

  const cities = [
    { name: 'Москва', isActive: true },
    { name: 'Санкт-Петербург', isActive: false },
    { name: 'Подмосковье', isActive: false },
  ]

  const menuItems = [
    { name: 'Лофты' },
    { name: 'Залы' },
    { name: 'Мероприятия' },
    { name: 'Внутри' },
    { name: 'Кейтеринг' },
    { name: 'О нас' },
    { name: 'Журнал' },
    { name: 'Контакты' },
  ]

  onMounted(() => {
    const split = new SplitText([locations.value, menu.value], {
      type: 'lines',
      linesClass: 'line',
    })

    gsap
      .timeline()
      .from(logo.value, {
        opacity: 0,
        x: -50,
        duration: 0.5,
        delay: 1,
      })
      .from(split.lines, {
        opacity: 0,
        x: -50,
        duration: 0.5,
      })
  })
</script>

<style scoped lang="scss"></style>
