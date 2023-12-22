<template>
    <div class="flex items-center gap-4">
        <p class="text-3xl"><span class="text-[#C778DD]">#</span>{{ title }}</p>
        <span v-if="decoration" class="title-dec"></span>
    </div>
</template>

<script>
export default {
    props: {
        title: {
            required: true,
        },
        decoration: {
            required: false,
        }
    }
}
</script>

<style scoped>
p {
    position: relative;
}

.title-dec {
    content: '';
    width: 100%;
    height: 1px;
    display: block;
    background: #C778DD;
    top: 50%;
    transform: translateY(-50%);
}
</style>