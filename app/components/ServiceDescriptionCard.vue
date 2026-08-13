<script setup lang="ts">
defineProps<{
    icon: string;
    title: string;
    description: string;
    items: string[];
}>();
</script>

<template>
    <Reveal
        class="bg-white rounded-xl shadow-md p-8 hover:shadow-xl transition-shadow border-t-4 border-transparent hover:border-eng-light">
        <div class="w-14 h-14 bg-blue-50 rounded-lg flex items-center justify-center mb-6 text-eng-primary">
            <ClientOnly>
                <Icon :name="icon" class="w-8 h-8" />
            </ClientOnly>
        </div>
        <h3 class="text-2xl font-bold text-eng-dark mb-3">{{ title }}</h3>
        <p class="text-gray-600 mb-4">{{ description }}</p>
        <ul class="text-sm text-gray-500 space-y-2">
            <li v-for="value in items" class="flex items-center">
                <Icon name="mdi:check" class="w-4 h-4 text-green-500 mr-2" />
                <span>{{ value }}</span>
            </li>
        </ul>
    </Reveal>
</template>