<template>
    <a :href="link" class="py-[8px] px-[16px] border border-[#C778DD] inline-block hover:bg-[#C778DD] hover:cursor-pointer hover:bg-opacity-20 transition-colors">
        <slot></slot>
    </a>
</template>

<script>
export default {
    props: {
        link: {
            required: true,
        }
    }
}
</script>