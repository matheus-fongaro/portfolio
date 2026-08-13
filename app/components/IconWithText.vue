<script setup lang="ts">
defineProps<{
    icon: string;
    title: string;
    description: string;
}>();
</script>

<template>
    <Reveal>
        <div class="p-4">
            <div class="text-eng-light mb-3 flex justify-center">
                <ClientOnly>
                    <Icon :name="icon" class="w-10 h-10" />
                </ClientOnly>
            </div>
            <h3 class="text-xl font-bold text-eng-dark mb-2">{{ title }}</h3>
            <p class="text-gray-600 text-sm">{{ description }}</p>
        </div>
    </Reveal>
</template>