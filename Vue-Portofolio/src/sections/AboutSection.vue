<script setup>
import HeaderTitle from '@/components/HeaderTitle.vue';

import profPic from '@/assets/img/aldo.jpeg';

import VLazyImage from 'v-lazy-image';
</script>

<template>
  <!-- Start About Section -->
  <kinesis-container tag="section" class="about" id="aboutSection">
    <!-- Pattern Group -->
    <div class="pattern">
      <kinesis-element :strength="75" class="ornament ornament__ellipse-1"></kinesis-element>
    </div>

    <div class="container">
      <div class="left">
        <div class="left__text" v-motion-slide-visible-once-left>
          <HeaderTitle titleMsg="About Me" />
          <div class="img-tablet">
            <v-lazy-image :src="profPic" :src-placeholder="profPicUnload" alt="Profile Picture" />
          </div>
          <p class="text-md">
            Halo saya Aldo Pratama. Saya lahir di daerah duri, 23 Juni 2003. Sekarang saya pendidikan menjadi Mahasiswa di Universitas Islam Riau. Saya memilliki kemampuan komunikasi yang cukup baik, critical thinking. Dan Saya memiliki sedikit pengalaman yaitu Introduction of Cyber Security dan Introduction Penetration Testing walapun itu hanya fundamental dijenjang cyber security
          </p>
        </div>
        <a href="" class="btn btn--primary btn--md left__btn" target="_blank" v-motion-slide-visible-once-bottom>Start</a>
      </div>

      <kinesis-element :strength="-20" type="depth_inv" class="right">
        <v-lazy-image :src="profPic" :src-placeholder="profPicUnload" alt="Profile Picture" v-motion-slide-visible-once-right />
      </kinesis-element>
    </div>
  </kinesis-container>
  <!-- End About Section -->
</template>

<style lang="scss" scoped>
@import '@/assets/scss/styles.scss';

section.about#aboutSection {
  // Pattern Settings
  .pattern {
    .ornament__ellipse-1 {
      width: 580px;
      height: 580px;
      left: -290px;
      top: 46px;
      background: #5d008a;
    }
  }
  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;

    @include media-breakpoint-down(md) {
      flex-direction: column;
      gap: toRem(56);
    }

    img {
      border-radius: 10px;
    }

    .left {
      max-width: 396px;
      display: flex;
      flex-direction: column;
      gap: toRem(32);

      @include media-breakpoint-down(md) {
        max-width: 100%;
        align-items: center;
        text-align: center;
      }

      &__text {
        display: flex;
        flex-direction: column;
        gap: toRem(16);

        @include media-breakpoint-down(md) {
          gap: toRem(56);
          align-items: center;
        }

        @include media-breakpoint-down(xs-2) {
          gap: toRem(32);
        }

        .img-tablet {
          width: 100%;

          @include media-breakpoint-up(md) {
            display: none;
          }

          img {
            width: 100%;
            height: auto;
          }
        }
      }

      &__btn {
        width: -moz-fit-content;
        width: fit-content;

        @include media-breakpoint-down(xs-2) {
          width: 100%;
        }
      }
    }

    .right {
      width: 400px;
      height: 400px;
      overflow: hidden;
      border-radius: 8px;
      display: flex;
      align-items: center;
      justify-content: center;

      img {
        width: auto;
        height: 400px;
      }

      @include media-breakpoint-down(md) {
        display: none;
      }
    }
  }
}
</style>
