<script setup lang="ts">
import Profile from './components/Profile.vue'
import Nav from './components/Nav.vue'
import Companies from './components/Companies.vue'
import Works from './components/Works.vue'
import Footer from './components/Footer.vue'
import { Separator } from '@/components/ui/separator'
import projects from './data/projects.json'
</script>

<template>
  <div class="flex h-screen flex-col justify-between">
    <div>
      <Nav />
      <Profile />
      <Companies />
      <div class="mx-10 mt-10">
        <Separator />
      </div>
      <Works :projects="projects" />
    </div>
    <Footer />
  </div>
</template>

<style scoped></style>