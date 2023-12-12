<template>
    <select 
        class="
            bg-transparent 
            text-gray-900
            rounded-lg 
            focus:ring-blue-500 
            focus:border-blue-500 
            p-2 
            dark:bg-[#282C33] 
            dark:border-gray-600 
            dark:placeholder-gray-400 
            dark:text-white 
            dark:focus:ring-blue-500 
            dark:focus:border-blue-500
            text-3xl
            lg:text-sm
            "
            @change="handleSelect"
            :value="selected"
    >
        <option
            v-for="locale in $i18n.availableLocales"
            v-bind:key="`locale-${locale}`"
            :value="locale"
        >
            {{ locale }}
        </option>
    </select>
</template>

<script>
import i18n from '../locales/i18n';

export default {
    data() {
        return {
            lang: i18n
        }
    },
    props: {
        options: {
            required: true,
        },
        selected: {
            required: true,
        }
    },
    methods: {
        handleSelect(event) {
            this.$emit('onSelect', event.target.value)
        }
    }
}
</script>