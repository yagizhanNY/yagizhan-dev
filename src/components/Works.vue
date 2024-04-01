<script setup lang="ts">
import {Project} from '../models/project'
import ProjectCard from './ProjectCard.vue'
    interface WorksProps{
        projects: Project[]
    }

    defineProps<WorksProps>();
</script>

<template>
    <div class="flex m-4">
        <div class="flex flex-col w-full items-end">
            <div>
                <h1 class="font-semibold text-[32px]">Works</h1>
                <div class="flex flex-col w-full">
                    <div>
                        <p class="max-w-[210px] font-light text-[13px]">Besides my full-time job, I also work on some side projects that I find
                            interesting, fun, helpful and
                            challenging.</p>
                        <a class="text-blue-500 underline font-light text-[13px]" href="https://github.com/yagizhanNY" target="_blank">Show all
                            projects &nearr;</a>
                    </div>

                </div>
            </div>
        </div>
        <div class="w-full ml-5">
            <div class="grid grid-cols-1 lg:grid-cols-2 max-w-[550px]">
                <template v-for="project of projects">
                    <ProjectCard :project="project"/>
                </template>
            </div>
        </div>
    </div>
</template>