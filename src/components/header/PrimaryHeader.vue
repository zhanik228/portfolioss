<template>
    <header class="containerr mx-auto flex py-3 items-center gap-4">
        <div class="left-links hidden sm:left-2 sm:absolute lg:flex top-0 flex-col items-center">
            <div class="line h-[191px] bg-white w-[1px] mb-4"></div>
            <ul class="flex flex-col items-center gap-4 h-[64px]">
                <li>
                    <a target="_blank" href="https://github.com/zhanik228">
                        <img width="21" height="20" src="@/assets/Vectorgithub.svg" alt="">
                    </a>
                </li>
                <li>
                    <a target="_blank" href="https://t.me/Lvh2288">
                        <img width="21" height="20" src="@/assets/Vectortelegram.svg" alt="">
                    </a>
                </li>
            </ul>
        </div>
        <div class="logo flex gap-2 font-bold flex-grow">
            <img src="@/assets/Logo.svg" alt="Logo" width="16">
            <a href="#"><h1>{{ $t('author') }}</h1></a>
        </div>
        <primary-nav :items="navLinks" />
        <primary-select class="hidden lg:block" :selected="selectedLang" @onSelect="onSelect" :options="options" />
    </header>
</template>

<script>
import PrimaryNav from '@/components/nav/PrimaryNav.vue'
import PrimarySelect from '@/components/select/PrimarySelect.vue'
import i18n from '../locales/i18n'

export default {
    components: {
        PrimaryNav,
        PrimarySelect
    },
    data() {
        return {
            navLinks: [],
            selectedLang: localStorage.getItem('lang'),
            options: [
                {
                    name: 'En',
                    value: 'en',
                },
                {
                    name: 'Ru',
                    value: 'ru',
                },
            ]
        }
    },
    methods: {
        onSelect(event) {
            console.log(event)
            localStorage.setItem('lang', event)
            window.location.reload()
        }
    },
    mounted() {
        console.log(this.navLinks = i18n.global.messages[i18n.global.locale].navLinks)

    }
}
</script>

<style>

</style>