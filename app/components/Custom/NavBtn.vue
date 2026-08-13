<script setup lang="ts">
defineProps<{
    text: string;
    anchor: string;
}>();
</script>

<template>
    <NuxtLink :to="anchor" class="hover:text-eng-light transition-colors text-sm font-medium">{{ text }}</NuxtLink>
</template>