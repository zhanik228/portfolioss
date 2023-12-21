<template>
  <main class="mx-auto">
    <intro-view />
    <project-section />
  </main>
</template>

<script>
import IntroView from '@/views/IntroView.vue'
import ProjectSection from "@/views/ProjectSection.vue"

export default {
  components: { IntroView, ProjectSection },
}
</script>