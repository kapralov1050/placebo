<template>
  <section
    class="w-full flex justify-end items-center space-x-5 py-8 px-7 fixed z-10"
  >
    <a
      class="font-semibold text-sm text-neutral-200"
      href="tel:88005553535"
      ref="phone"
    >
      8 800 555-35-35
    </a>
    <button
      class="px-6 py-2 bg-white text-black rounded-xl hover:bg-neutral-200"
      ref="callButton"
    >
      Перезвоните мне
    </button>
  </section>
</template>

<script setup>
  import { ref, onMounted } from 'vue'
  import gsap from 'gsap'

  const phone = ref(null)
  const callButton = ref(null)

  onMounted(() => {
    gsap
      .timeline()
      .from(phone.value, {
        opacity: 0,
        y: 50,
        duration: 0.5,
        delay: 1.5,
      })
      .from(callButton.value, {
        opacity: 0,
        y: 50,
        duration: 0.5,
      })
  })
</script>

<style scoped lang="scss"></style>
