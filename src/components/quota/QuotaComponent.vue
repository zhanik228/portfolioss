<template>
    <section class="my-20 flex justify-center quota-section">
        <div class="containerr w-[80%] flex flex-col items-end">
            <p class="mx-auto relative border p-8 block text-2xl">
                <img src="@/assets/quota.png" alt="quota" class="absolute top-[-20px]">
                <img src="@/assets/quota.png" alt="quota" class="absolute bottom-[-20px] right-5">
                {{ quota }}
                <span class="absolute top-full right-[-1px] border border-t-0 p-4 block">{{ quotaAuthor }}</span>
            </p>
        </div>
    </section>
</template>

<script>
export default {
    props: {
        quota: {
            required: true,
        },
        quotaAuthor: {
            required: true,
        }
    }
}
</script>