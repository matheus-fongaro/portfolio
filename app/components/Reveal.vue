<script setup lang="ts">
const el = ref < HTMLElement | null > (null);
const isVisible = ref(false);

onMounted(() => {
    const observer = new IntersectionObserver(
        ([entry]) => {
            if (entry?.isIntersecting) {
                isVisible.value = true;
                observer.disconnect();
            }
        },
        {
            threshold: 0.15,
            rootMargin: '0px 0px -30px 0px',
        }
    )

    if (el.value) observer.observe(el.value);

    onBeforeUnmount(() => observer.disconnect());
})
</script>

<template>
    <div ref="el"
        :class="['transition-all duration-700 ease-out', isVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-10']">
        <slot />
    </div>
</template>