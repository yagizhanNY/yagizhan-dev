<script setup lang="ts">
interface CompanyInfoProps {
    logoName: string;
    alt: string;
    date: string;
    websiteLink: string;
}

defineProps<CompanyInfoProps>();
</script>

<template>
    <div class="flex justify-center mt-5">
        <div class="flex-row items-center justify-center">
            <a class="group flex h-10 w-20 items-center justify-center" :href="websiteLink" target="_blank">
                <img class="transition duration-300 ease-in-out group-hover:-translate-y-1.5" loading="lazy" height="140" width="90" :src="`../assets/img/${logoName}.png`" :alt="alt">
            </a>
            <p class="font-extralight text-center text-[10px]">{{ date }}</p>
        </div>
    </div>

</template>