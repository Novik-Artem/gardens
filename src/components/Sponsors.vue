<template>
  <div :class="$style.container">
    <div :class="$style.title">{{ $t("sponsorsSection.title") }}</div>
    <div :class="$style.sponsors">
      <div :class="$style.sponsor" v-for="item in sponsors" :key="item.text">
        <div :class="$style.content">
          <div :class="$style.logo">
            <img :src="item.image" alt="" />
          </div>
          <!-- <div :class="$style.text">
            {{ item.text }}
          </div> -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import dataEn from "../locales/en.json";
import dataPl from "../locales/pl.json";
export default {
  data() {
    return {
      dataEn: dataEn.sponsorsSection.sponsors,
      dataPl: dataPl.sponsorsSection.sponsors,
      sponsors: [],
    };
  },
  computed: {
    locale() {
      return this.$i18n.locale;
    },
  },
  mounted() {
    if (this.$i18n.locale === "en") {
      this.sponsors = this.dataEn;
    } else {
      this.sponsors = this.dataPl;
    }
  },
  watch: {
    locale() {
      if (this.$i18n.locale === "en") {
        this.sponsors = this.dataEn;
      } else {
        this.sponsors = this.dataPl;
      }
    },
  },
};
</script>

<style lang="scss" module>
.container {
  max-width: 50rem;
  margin: 0 auto;
  padding: 3rem 0;
  color: $black;
  .title {
    padding: 0 3rem;
    @include F64-900;
    text-align: center;
    margin: 0 0 3rem 0;
    @include custom(1080) {
      font-size: 3rem;
    }
    @include custom(750) {
      font-size: 2rem;
      line-height: 100%;
    }
  }
  .sponsor {
    &:last-child {
      border-bottom: none;
      padding-bottom: 0;
    }
    .content {
      padding: 0 3rem;
      .logo {
        display: flex;
        justify-content: center;

        & img {
          width: 20rem;
          height: 20rem;
          object-fit: contain;
          @include custom(540) {
            width: 8rem;
            height: 8rem;
          }
        }
      }
      // .text {
      //   text-align: center;
      //   font-size: 1.3rem;
      //   line-height: 100%;
      // }
    }
  }
  .sponsors {
    display: flex;
    align-items: center;
    justify-content: center;
    @include custom(750) {
      flex-direction: column;
    }
  }
}
</style>
