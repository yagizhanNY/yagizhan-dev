<script setup lang="ts">
import { Project } from '@/models/project';

interface ProjectCardProps {
    project: Project
}

defineProps<ProjectCardProps>();
</script>

<template>
    <a class="w-40 h-44 lg:w-60 lg:h-48 mb-4 border shadow-md transition hover:duration-300 hover:ease-in-out hover:-translate-y-1.5" :href="project.projectUrl">
        <div class="flex min-h-24 min-w-24 justify-center items-center">
            <img :src="`/${project.imageUrl}.png`" :alt="project.imageUrl">
        </div>
        <p class="mx-2">{{ project.description }}</p>
    </a>
</template>