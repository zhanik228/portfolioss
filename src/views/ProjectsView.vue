<template>
    <div class="containerr mx-auto my-5 mb-9">
        <h2 class="text-2xl mb-3"><span class="text-[#C778DD]">/</span> Projects</h2>
        <p>List of my projects</p>
    </div>
    <section-title class="containerr mx-auto" title="complete apps"/>
    <primary-card-list class="containerr mx-auto my-4" :cards="cards" />
</template>

<script>
import SectionTitle from '@/components/section/SectionTitle.vue';
import PrimaryCardList from '@/components/card/PrimaryCardList.vue';

export default {
    components: {
        SectionTitle,
        PrimaryCardList
    },
    data() {
        return {
            cards: [
              {
                img: null,
                stack: ['HTML', 'CSS', 'PYTHON', 'FLASK'],
                title: 'ChertNodes',
                subtitle: 'Minecraft servers hosting',
                live: null,
                github: 'https://github.com/zhanik228',
              },
              {
                img: null,
                stack: ['HTML', 'CSS', 'PYTHON', 'FLASK'],
                title: 'ChertNodes',
                subtitle: 'Minecraft servers hosting',
                live: null,
                github: 'https://github.com/zhanik228',
              },
              {
                img: null,
                stack: ['HTML', 'CSS', 'PYTHON', 'FLASK'],
                title: 'ChertNodes',
                subtitle: 'Minecraft servers hosting',
                live: null,
                github: 'https://github.com/zhanik228',
              }
            ]
        }
    }
}
</script>