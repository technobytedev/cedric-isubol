<template>
    <div class="grid grid-cols-4 gap-4 mt-12">
        <template v-for="(image, index) in gallery" :key="index">
            <div class="col-span-full md:col-span-4 lg:col-span-4 group mx-auto max-w-[800px] h-full">
                <Image :src="image.url" :alt="image.alt" class="pt-10" />
            </div>
        </template>
    </div>
</template>

<script setup>
const app = useAppConfig();
const { data: { gallery } } = app
</script>
