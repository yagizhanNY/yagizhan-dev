<script lang="ts" setup>
import { Icon } from '@iconify/vue'

export interface LinkProp {
  title: string
  label?: string
  icon: string
  variant: 'default' | 'ghost'
}

interface NavProps {
  isCollapsed: boolean
  links: LinkProp[]
}

defineProps<NavProps>()
</script>

<template>
  <div>
    <nav class="flex-row px-4 mt-4 gap-3">
      <template v-for="link of links">
        <div class="flex items-center text-white rounded-md bg-black gap-2 px-3 py-1">
          <Icon :icon="link.icon" />
          <p>{{ link.title }}</p>
        </div>
      </template>
    </nav>
  </div>
</template>