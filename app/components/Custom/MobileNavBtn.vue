<script setup lang="ts">
defineProps<{
    text: string;
    anchor: string;
}>();
</script>

<template>
    <NuxtLink :to="anchor" class="block px-3 py-2 text-base font-medium hover:text-eng-light">{{ text }}</NuxtLink>
</template>