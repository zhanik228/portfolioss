<template>
  <main class="mx-auto">
    <intro-view />
    <quota-component :quota="$t('intro.quota')" :quotaAuthor="$t('intro.quota-author')" />
    <project-section />
  </main>
  <primary-footer class="my-5" />
</template>

<script>
import IntroView from '@/views/IntroView.vue'
import ProjectSection from "@/views/ProjectSection.vue"
import QuotaComponent from '@/components/quota/QuotaComponent.vue'
import PrimaryFooter from '@/components/footer/PrimaryFooter.vue'

export default {
  components: { IntroView, ProjectSection, QuotaComponent, PrimaryFooter },
}
</script>,
    QuotaComponent