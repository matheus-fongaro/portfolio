<script setup lang="ts">
defineProps<{
    image: string;
    title: string;
    tag: string;
}>();
</script>

<template>
    <Reveal class="group rounded-xl overflow-hidden shadow-lg bg-white border border-gray-100">
        <div class="relative h-64 overflow-hidden bg-gray-200">
            <ClientOnly>
                <NuxtImg :src="image"
                    class="w-full h-full object-cover transform group-hover:scale-105 transition-transform duration-500" />
                <div class="absolute top-4 right-4 bg-eng-dark text-white text-xs font-bold px-3 py-1 rounded">{{ tag
                    }}
                </div>
            </ClientOnly>
        </div>
        <div class="p-6">
            <h3 class="text-2xl font-bold text-eng-dark mb-2">{{ title }}</h3>
            <slot />
        </div>
    </Reveal>
</template>