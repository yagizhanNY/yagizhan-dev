<script setup lang="ts">
import CompanyInfo from './CompanyInfo.vue'
</script>

<template>
    <div class="w-full flex-row justify-center items-center mt-10">
        <p class="font-extralight text-center">I've worked with great companies and still do</p>
        <div class="flex justify-center items-center gap-20">
            <CompanyInfo :logo-name="'km'" :alt="'Kontrolmatik Technologies'" :date="'06.2017 - 10.2021'" :website-link="'https://www.kontrolmatik.com/'"/>
            <CompanyInfo :logo-name="'siemens'" :alt="'Siemens'" :date="'10.2021 - now'" :website-link="'https://www.siemens.com/global/en.html'"/>
        </div>
    </div>
</template>