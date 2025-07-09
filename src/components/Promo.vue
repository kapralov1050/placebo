<template>
  <section
    class="w-full h-screen flex flex-col justify-center items-center
      bg:overflow-hidden bg-right bg-cover bg-no-repeat
      bg-[url(./assets/Promo.png)] bg-black after:content after:w-full
      after:h-[30vh] after:absolute after:top-190 after:bg-linear-to-t
      after:from-black after:from-60% after:to-transparent after:to-100%"
  >
    <h1
      ref="titleElement"
      class="font-lithium leading-[0.9] text-4xl scale-y-180 tracking-widest
        text-center max-w-80 mb-16"
    >
      АВТОРСКИЕ EVENT-ПРОСТРАНСТВА В МОСКВЕ
    </h1>
    <p
      ref="descriptionElement"
      class="text-center max-w-90 text-neutral-400 mb-20"
    >
      Первоклассный сервис, изысканная кухня, стильные интерьеры и полное
      техническое оснащение
    </p>
  </section>
</template>

<script setup>
  import { ref, onMounted } from 'vue'
  import gsap from 'gsap'
  import { SplitText } from 'gsap/SplitText'

  gsap.registerPlugin(SplitText)

  const titleElement = ref(null)
  const descriptionElement = ref(null)

  onMounted(() => {
    const split = new SplitText(titleElement.value, {
      type: 'lines',
      linesClass: 'line',
    })

    gsap
      .timeline()
      .from(split.lines, {
        opacity: 0,
        y: 50,
        duration: 0.5,
      })
      .from(descriptionElement.value, {
        opacity: 0,
        y: 50,
        duration: 0.5,
      })
  })
</script>
