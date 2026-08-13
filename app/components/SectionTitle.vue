<script setup lang="ts">
defineProps<{
    title: string;
    description: string;
}>();
</script>

<template>
    <Reveal>
        <div class="text-center max-w-3xl mx-auto mb-16">
            <h2 class="text-3xl md:text-4xl font-bold text-eng-dark mb-4">{{ title }}
            </h2>
            <div class="h-1 w-20 bg-eng-light mx-auto mb-6"></div>
            <p class="text-gray-600 text-lg">{{ description }}</p>
        </div>
    </Reveal>
</template>