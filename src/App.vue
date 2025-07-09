<script setup>
  import Promo from './components/Promo.vue'
  import Sidebar from './components/Sidebar.vue'
  import Header from './components/Header.vue'
  import Filters from './components/Filters.vue'
  import PlacesList from './components/PlacesList.vue'
  import Announce from './components/Announce.vue'
  import Footer from './components/Footer.vue'
</script>

<template>
  <Sidebar />
  <header>
    <Header />
    <Promo />
  </header>
  <main class="w-full bg-black flex flex-col justify-start items-center mb-25">
    <Filters />
    <PlacesList />
    <Announce />
  </main>
  <footer class="w-full bg-black flex flex-col items-center">
    <Footer />
  </footer>
</template>

<style scoped></style>
