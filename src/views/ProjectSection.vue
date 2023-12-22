<template>
    <div class="containerr mx-auto">
      <section class="flex justify-between items-center">
        <section-title class="my-4 basis-3/4" :title="$t('project-section.title')" :decoration="true" />
        <router-link to="/projects">{{ $t('project-section.see-more') }} ~~></router-link>
      </section>
        <primary-card-list :cards="cards" />
    </div>
</template>


<script>
import SectionTitle from '@/components/section/SectionTitle.vue'
import img from "@/assets/Rectangle 22.jpg"
import PrimaryCardList from '@/components/card/PrimaryCardList.vue'
import { RouterLink } from 'vue-router'

export default {
  components: { SectionTitle, PrimaryCardList, RouterLink },
  data() {
    return {
      cards: [
        {
          img: img,
          stack: ['HTML', 'CSS', 'PYTHON', 'FLASK'],
          title: 'ChertNodes',
          subtitle: 'Minecraft servers hosting',
          live: null,
          github: 'https://github.com/zhanik228',
        },
        {
          img: img,
          stack: ['HTML', 'CSS', 'PYTHON', 'FLASK'],
          title: 'ChertNodes',
          subtitle: 'Minecraft servers hosting',
          live: null,
          github: 'https://github.com/zhanik228',
        },
        {
          img: img,
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