<script setup>
import HeaderTitle from '@/components/HeaderTitle.vue';
import ProjectLists from '@/components/ProjectCards.vue';
</script>

<template>
  
</template>

<style lang="scss" scoped>
@import '@/assets/scss/styles.scss';

section.projects#projectSection {
  height: 1338px;

  @include media-breakpoint-down(lg) {
    height: auto;
  }
  // Pattern Settings
  .pattern {
    .ornament__ellipse-1 {
      width: 291px;
      height: 291px;
      left: -121px;
      top: 1097px;
      background: #0354e2;
    }
  }
  .container {
    display: flex;
    flex-direction: column;
    gap: toRem(32);
    align-items: center;

    .btn {
      @include media-breakpoint-down(xs-2) {
        width: 100%;
      }
    }
  }
}
</style>