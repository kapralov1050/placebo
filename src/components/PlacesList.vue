<template>
  <section class="w-2/3 grid grid-cols-3 gap-x-5 gap-y-5 px-5">
    <PlaceCard v-for="place in places" :place="place" />
  </section>
</template>

<script setup>
  import PlaceCard from './PlaceCard.vue'

  const places = [
    {
      id: 1,
      name: 'Rockefellers Hall',
      image: '../../public/image1.png',
      area: 800,
      capacity: [200, 400],
      location: 'м.Павелецкая',
    },
    {
      id: 2,
      name: 'Grace Hall',
      image: '../../public/image2.png',
      area: 800,
      capacity: [200, 400],
      location: 'м.Павелецкая',
    },
    {
      id: 3,
      name: 'Montblanc Hall',
      image: '../../public/image3.png',
      area: 800,
      capacity: [200, 400],
      location: 'м.Павелецкая',
      description:
        'Первоклассный сервис, изысканная кухня, стильные интерьеры и полное техническое оснаис, изысканная кухня, стильные интерьеры и полное техническое оснащение\n\nПервоклассный сервис, изысканная кухня, стильные интерьеры и полное техническое оснащение',
    },
    {
      id: 4,
      name: 'Rockefellers Hall',
      image: '../../public/image1.png',
      area: 800,
      capacity: [200, 400],
      location: 'м.Павелецкая',
    },
    {
      id: 5,
      name: 'Grace Hall',
      image: '../../public/image2.png',
      area: 800,
      capacity: [200, 400],
      location: 'м.Павелецкая',
    },
    {
      id: 6,
      name: 'Montblanc Hall',
      image: '../../public/image4.png',
      area: 800,
      capacity: [200, 400],
      location: 'м.Павелецкая',
    },
  ]
</script>

<style scoped lang="scss"></style>
