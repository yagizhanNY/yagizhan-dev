<script setup lang="ts">
import {Project} from '../models/project'
    interface WorksProps{
        projects: Project[]
    }

    defineProps<WorksProps>();
</script>

<template>
    <div class="flex">
        <div class="flex flex-col w-full items-center">
            <div>
                <h1 class="font-semibold text-[32px]">Works</h1>
                <div class="flex flex-col w-full items-center">
                    <div>
                        <p class="max-w-[236px] font-light text-[13px]">Besides my full-time job, I also work on some side projects that I find
                            interesting, fun, helpful and
                            challenging.</p>
                        <a class="text-blue-500 underline font-light text-[13px]" href="https://github.com/yagizhanNY" target="_blank">Show all
                            projects &nearr;</a>
                    </div>

                </div>
            </div>

        </div>
        <div class="w-full">
            <div class="grid">
                <template v-for="project of projects">
                    <p>{{ project.description }}</p>
                </template>
            </div>
        </div>
    </div>
</template>