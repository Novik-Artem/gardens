<template>
  <div :class="$style.wrapper">
    <div :class="$style.container">
      <div :class="$style.title">{{ $t("developmentSection.title") }}</div>
      <div :class="$style.content">
        <div :class="$style.column" v-for="item in cards" :key="item.title">
          <div :class="$style.subtitle">{{ item.title }}</div>
          <div :class="$style.text">{{ item.text }}</div>
        </div>
      </div>
      <video
        :class="$style.video"
        controls
        ref="video"
        src="/video/1.mp4"
        type="video/mp4"
      ></video>
    </div>
  </div>
</template>

<script>
import dataEn from "../locales/en.json";
import dataPl from "../locales/pl.json";
export default {
  data() {
    return {
      dataEn: dataEn.developmentSection.cards,
      dataPl: dataPl.developmentSection.cards,
      cards: [],
    };
  },
  computed: {
    locale() {
      return this.$i18n.locale;
    },
  },
  mounted() {
    if (this.$i18n.locale === "en") {
      this.cards = this.dataEn;
    } else {
      this.cards = this.dataPl;
    }
  },
  watch: {
    locale() {
      if (this.$i18n.locale === "en") {
        this.cards = this.dataEn;
      } else {
        this.cards = this.dataPl;
      }
    },
  },
};
</script>

<style lang="scss" module>
.wrapper {
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  background-image: url("../assets/images/bg2.png");
  @include custom(930) {
    background-image: none;
  }
  padding: 5.625rem 0;
  background-color: $light-brown;
  // margin-top: 5rem;
  .container {
    @include container;
    .title {
      @include F64-900;
      text-align: center;
      margin: 0 0 2rem 0;
      @include custom(1080) {
        font-size: 3rem;
      }
      @include custom(750) {
        font-size: 2.5rem;
        line-height: 100%;
      }
      @include custom(500) {
        font-size: 2rem;
        margin: 0 0 1rem 0;
        line-height: 100%;
      }
    }
    .content {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 1.5rem;
      margin: 0 0 10rem 0;
      @include custom(1010) {
        margin: 0 0 8rem 0;
      }
      @include custom(670) {
        margin: 0 0 5rem 0;
      }
      @include custom(970) {
        grid-template-columns: 1fr 1fr;
        .column:last-child {
          grid-column: 1/ -1;
        }
      }
      @include custom(660) {
        display: block;
        .column {
          margin: 0 0 2rem 0;
        }
        .column:last-child {
          margin: 0;
        }
      }
      .subtitle {
        @include F36-600;
        @include custom(1060) {
          font-size: 1.8rem;
        }
      }
      .text {
        @include F28-400;
        @include custom(1060) {
          font-size: 1.5rem;
        }
      }
    }
    .video {
      object-fit: cover;
      width: 100%;
      height: 100%;
      border-radius: 1.25rem;
      margin-bottom: -15rem;
      max-width: 88.25rem;
      height: 42.375rem;
      @include custom(1010) {
        height: 30rem;
        margin-bottom: -10rem;
      }
      @include custom(670) {
        height: 20rem;
        margin-bottom: 0;
      }
    }
  }
}
</style>
