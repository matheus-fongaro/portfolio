<script setup lang="ts">
const showMobileMenu = ref(false);
function changeShowMobileMenu() {
    showMobileMenu.value = !showMobileMenu.value;
}
</script>

<template>
    <nav class="bg-eng-dark text-white fixed w-full z-50 top-0 shadow-lg transition-all duration-300" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-20 items-center">
                <NuxtLink to="/" class="flex-shrink-0 flex items-center gap-2 cursor-pointer">
                    <Icon name="lucide:building-2" class="w-8 h-8 text-eng-light" />
                    <span class="font-bold text-xl tracking-tight">Matheus Fongaro <span
                            class="text-eng-light">Engenheiro Civil</span></span>
                </NuxtLink>
                <!-- desktop menu -->
                <div class="hidden md:flex space-x-8 items-center">
                    <CustomNavBtn text="Sobre" anchor="#sobre" />
                    <CustomNavBtn text="Serviços" anchor="#servicos" />
                    <CustomNavBtn text="Portfólio" anchor="#portfolio" />
                    <NuxtLink
                        class="bg-eng-light text-eng-dark px-5 py-2 rounded-md font-semibold hover:bg-white transition-colors text-sm"
                        to="#contato">Falar no WhatsApp</NuxtLink>
                </div>
                <!-- mobile menu btn -->
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-btn" class="text-white hover:text-eng-light focus:outline-none"
                        @click="changeShowMobileMenu">
                        <Icon name="lucide:menu" class="w-6 h-6" />
                    </button>
                </div>
            </div>
        </div>
        <!-- mobile menu content -->
        <div v-show="showMobileMenu" id="mobile-menu" class="md:hidden bg-eng-primary">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
                <CustomMobileNavBtn text="Sobre" anchor="#sobre" @click="changeShowMobileMenu" />
                <CustomMobileNavBtn text="Serviços" anchor="#servicos" @click="changeShowMobileMenu" />
                <CustomMobileNavBtn text="Portfólio" anchor="#portfolio" @click="changeShowMobileMenu" />
                <NuxtLink class="block px-3 py-2 text-base font-medium text-eng-light" to="#contato" @click="changeShowMobileMenu">
                    Falar no WhatsApp
                </NuxtLink>
            </div>
        </div>
    </nav>
</template>