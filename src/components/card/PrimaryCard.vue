<template>
    <div v-if="card" class="border border-[#ABB2BF]">
        <img v-if="card.img" class="block w-full" :src="card.img" alt="card img">
        <div class="border-top border-b flex gap-2 p-2">
            <span class="text-[#ABB2BF]" v-for="sItem in card.stack" :key="sItem">
                {{ sItem }}
            </span>
        </div>
        <div class="p-2">
            <h2 class="text-2xl">{{ card.title }}</h2>
            <p class="text-[#ABB2BF]">{{ card.subtitle }}</p>
        </div>
        <div class="p-2 flex justify-between">
            <primary-button v-if="card.live">Live &lt~></primary-button>
            <primary-button :link="card.github" v-if="card.github">Github &lt~></primary-button>
        </div>
    </div>
</template>

<script>
import PrimaryButton from "../button/PrimaryButton.vue"

export default {
  components: { PrimaryButton },
    props: {
        card: {
            required: true,
        }
    }
}
</script>