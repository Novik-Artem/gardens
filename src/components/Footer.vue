<template>
  <footer :class="$style.footer">
    <div :class="$style.content">
      <div :class="$style.links">
        <div
          v-for="item in links.first"
          :key="item.text"
          :class="$style.link"
          @click="scrollTo('#' + item.id)"
        >
          {{ item.text }}
        </div>
      </div>
      <div :class="$style.links">
        <div
          v-for="item in links.second"
          :key="item.text"
          :class="$style.link"
          @click="scrollTo('#' + item.id)"
        >
          {{ item.text }}
        </div>
      </div>
      <div :class="$style.links">
        <div
          v-for="item in links.third"
          :key="item.text"
          :class="$style.link"
          @click="scrollTo('#' + item.id)"
        >
          {{ item.text }}
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import dataEn from "../locales/en.json";
import dataPl from "../locales/pl.json";
import VueScrollTo from "vue-scrollto";
export default {
  data() {
    return {
      dataEn: dataEn.footer.links,
      dataPl: dataPl.footer.links,
      links: {
        first: [],
        second: [],
        third: [],
      },
    };
  },
  computed: {
    locale() {
      return this.$i18n.locale;
    },
  },
  mounted() {
    if (this.$i18n.locale === "en") {
      this.links.first = this.dataEn.first;
      this.links.second = this.dataEn.second;
      this.links.third = this.dataEn.third;
    } else {
      this.links.first = this.dataPl.first;
      this.links.second = this.dataPl.second;
      this.links.third = this.dataPl.third;
    }
  },
  watch: {
    locale() {
      if (this.$i18n.locale === "en") {
        this.links.first = this.dataEn.first;
        this.links.second = this.dataEn.second;
        this.links.third = this.dataEn.third;
      } else {
        this.links.first = this.dataPl.first;
        this.links.second = this.dataPl.second;
        this.links.third = this.dataPl.third;
      }
    },
  },
  methods: {
    scrollTo(component) {
      VueScrollTo.scrollTo(component, {
        offset: -50,
        duration: 500,
      });
    },
  },
};
</script>

<style lang="scss" module>
.footer {
  height: 100%;
  width: 100%;
  background-repeat: no-repeat;
  background-size: cover;
  background-image: url("../assets/images/footer.png");
  .content {
    max-width: 60rem;
    margin: 0 auto;
    padding: 6.25rem 1rem;
    position: relative;
    z-index: 2;
    display: grid;
    align-items: center;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 5rem;
    @include custom(840) {
      gap: 1rem;
    }
    @include custom(535) {
      padding: 3rem 1rem;
    }
    @include custom(470) {
      grid-template-columns: 1fr;
      gap: 0;
    }
    .links {
      .link {
        margin: 0 0 1rem 0;
        transition: all 0.3s ease-in-out;
        &:hover {
          color: $orange;
        }
        &:last-child {
          margin: 0;
        }
        cursor: pointer;
        color: $white;
        @include F28-500;
        @include custom(840) {
          font-size: 1.25rem;
        }
        @include custom(535) {
          font-size: 1.08rem;
        }
        @include custom(470) {
          text-align: center;
        }
      }
    }
  }
}
</style>
