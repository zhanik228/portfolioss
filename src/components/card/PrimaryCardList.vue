<template>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
        <primary-card :card="card" v-for="card in cards" :key="card.title" />
    </div>
</template>

<script>
import PrimaryCard from './PrimaryCard.vue'
export default {
  components: { PrimaryCard },
    props: {
        cards: {
            required: true,
        }
    }
}
</script>