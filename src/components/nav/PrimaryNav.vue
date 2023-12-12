<template>
    <nav class="hidden lg:block">
        <ul class="flex gap-4">
            <li v-for="link in items" v-bind:key="link.name">
                <a
                    data-prefix="#"
                    :href="'#' + link.name"
                    :class="
                            link.isSelected ?
                            'active'
                            : ''
                    "
                >
                    {{ link.name }}
                </a>
            </li>
        </ul>
    </nav>
    <button @click="toggle" class="nav-toggle lg:!hidden">
        <span class="bar"></span>
        <span class="bar"></span>
    </button>
    <div :class="`${isNavOpen ? 'left-0 ' : 'left-[-150%] '} z-50 lg:hidden bg-[#282C33] w-full transition-all absolute top-[48px] bottom-0 end-0 start-0 flex flex-col justify-center items-center p-4 gap-2`">
        <div class=" flex flex-col flex-grow items-center justify-center">
        <nav class="">
            <ul class="flex flex-col gap-20">
                <li v-for="link in items" v-bind:key="link.name">
                    <a
                        data-prefix="#"
                        :href="'#' + link.name"
                        :class="`
                                ${link.isSelected ?
                                'active '
                                : ''}
                                text-5xl
                        `"
                    >
                        {{ link.name }}
                    </a>
                </li>
            </ul>
        </nav>
    <primary-select class="self-start mt-4" :selected="selectedLang" @onSelect="onSelect" :options="options" />
        </div>
    <ul class="flex items-center gap-4 h-[64px]">
        <li>
            <a target="_blank" href="https://github.com/zhanik228">
                <img width="42" height="40" src="@/assets/Vectorgithub.svg" alt="">
            </a>
        </li>
        <li>
            <a target="_blank" href="https://t.me/Lvh2288">
                <img width="42" height="40" src="@/assets/Vectortelegram.svg" alt="">
            </a>
        </li>
    </ul>
    </div>
</template>

<script>
import PrimarySelect from '@/components/select/PrimarySelect.vue'

export default {
    components: {
        PrimarySelect
    },
    props: {
        items: {
            required: true,
        }
    },
    data() {
        return {
            isNavOpen: false,
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
        },
        toggle() {
            this.isNavOpen = !this.isNavOpen
            console.log(this.isNavOpen)
        }
    },
}
</script>

<style scoped>
a {
    color: #ABB2BF;
}

a.active {
    color: #fff;
}

a:hover {
    color: #fff;
}

a[data-prefix]::before {
    content: attr(data-prefix);
    color: #C778DD;
}

.nav-toggle {
    width: 24px;
    height: 24px;
    display: flex;
    flex-direction: column;
    gap: 5px;
    cursor: pointer;
}

.bar {
    display: block;
    background-color: white;
    width: 100%;
    height: 2px;
}

.bar:last-child {
    width: 15px;
    align-self: end;
}
</style>