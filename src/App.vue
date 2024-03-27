<script setup lang="ts">
import Nav from './components/nav/Nav.vue';
import Profile from './components/Profile.vue'

const links: any[] = [
  {
    title: 'Home',
    icon: 'charm:north-star',
    variant: 'default',
  },
  {
    title: 'Drafts',
    icon: 'lucide:file',
    variant: 'ghost',
  },
  {
    title: 'Sent',
    icon: 'lucide:send',
    variant: 'ghost',
  }
]
</script>

<template>
  <div class="lg:flex h-screen">
    <div
      class="bg-zinc-50 scrollable-area relative w-full flex-col hidden lg:flex lg:flex-col lg:border-r lg:w-60 xl:w-72">
      <div>
        <Profile />
      </div>
      <Nav :links="links" :is-collapsed="false" />
    </div>
  </div>
</template>

<style scoped></style>