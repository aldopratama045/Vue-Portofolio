<script setup>
import SkillsLabel from '@/components/SkillsLabel.vue';
import HeaderTitle from '@/components/HeaderTitle.vue';
</script>

<template>
  <!-- Start Skills Section -->
  <kinesis-container tag="section" class="skills" id="skillsSection">
    <!-- Pattern Group -->
    <div class="pattern">
      <kinesis-element :strength="100" axis="y" class="ornament ornament__ellipse-1"></kinesis-element>
    </div>

    <div class="container">
      <div class="header">
        <HeaderTitle titleMsg="Skills"></HeaderTitle>
        <p class="text-md" v-motion-slide-visible-once-top>Saya mahir dan terbuka terhadap beberapa bahasa pemrograman, berikut ini adalah beberapa bahasa yang paling sering saya gunakan.</p>
      </div>
      <SkillsLabel />
    </div>
  </kinesis-container>
  <!-- End Skills Section -->
</template>

<style lang="scss" scoped>
@import '@/assets/scss/styles.scss';
section.skills#skillsSection {
  height: auto;

  // Pattern Settings
  .pattern {
    .ornament__ellipse-1 {
      width: 373px;
      height: 373px;
      left: 1239px;
      top: -135px;

      background: #0354e2;
    }
  }

  .container {
    padding: toRem(80) 0;
    display: flex;
    flex-direction: column;
    gap: toRem(32);

    @include media-breakpoint-down(sm) {
      padding: 0;
    }
  }
}
</style>
