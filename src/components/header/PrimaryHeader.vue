<template>
    <header class="containerr mx-auto flex py-3 items-center gap-4">
        <side-link />
        <div class="logo flex gap-2 font-bold flex-grow">
            <img src="@/assets/Logo.svg" alt="Logo" width="16">
            <router-link to="/"><h1>{{ $t('author') }}</h1></router-link>
        </div>
        <primary-nav :items="navLinks" />
        <primary-select class="hidden lg:block" :selected="selectedLang" @onSelect="onSelect" :options="options" />
    </header>
</template>

<script>
import PrimaryNav from '@/components/nav/PrimaryNav.vue'
import PrimarySelect from '@/components/select/PrimarySelect.vue'
import SideLink from '../side-link/SideLink.vue'

import i18n from '../locales/i18n'

export default {
    components: {
        PrimaryNav,
        PrimarySelect,
        SideLink
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