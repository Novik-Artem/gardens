<template>
  <div :class="$style.container">
    <div :class="$style.title">{{ $t("solutionSection.title") }}</div>
    <div :class="$style.content">
      <div :class="$style.column">
        <div :class="$style.item">
          <div :class="$style.subtitle">
            {{ $t("solutionSection.first.title") }}
          </div>
          <div :class="$style.text">
            {{ $t("solutionSection.first.text") }}
          </div>
          <div :class="$style.subtext">
            <li>{{ $t("solutionSection.first.firstItem.title") }}</li>
            <div>
              {{ $t("solutionSection.first.firstItem.text") }}
            </div>
          </div>
          <div :class="$style.subtext">
            <li>{{ $t("solutionSection.first.secondItem.title") }}</li>
          </div>
        </div>
        <Applicate :class="$style.app" />
      </div>
      <div :class="$style.column">
        <div :class="$style.item">
          <div :class="$style.image">
            <img src="/images/solution/1-horizontal.png" alt="" />
          </div>
          <div :class="$style.subtitle">
            {{ $t("solutionSection.second.title") }}
          </div>
          <div :class="$style.text">
            {{ $t("solutionSection.second.subtext") }}
          </div>
        </div>
        <Applicate :class="$style.adaptive" />
      </div>
    </div>
  </div>
</template>

<script>
import Applicate from "./Applicate.vue";
export default {
  components: {
    Applicate,
  },
};
</script>

<style lang="scss" module>
.container {
  @include container;
  // margin-bottom: 6.25rem;
  @include custom(720) {
    margin-bottom: 4rem;
  }
  .title {
    @include F64-900;
    margin: 0 0 6.25rem 0;
    text-align: center;
    @include custom(1050) {
      margin: 0 0 3rem 0;
    }
    @include custom(830) {
      font-size: 3rem;
      line-height: 100%;
    }
    @include mobile {
      font-size: 2.8rem;
    }
  }
  .content {
    // display: grid;
    // grid-template-columns: 1fr 1fr;
    // gap: 3rem;
    // justify-content: space-between;
    @include custom(875) {
      grid-template-columns: 1fr;
      gap: 1rem;
    }
    .column {
      .item {
        .subtitle {
          @include F36-600;
          line-height: 2rem;
          margin: 0 0 1.5rem 0;
          @include custom(1200) {
            font-size: 2rem;
            margin: 0 0 1rem 0;
          }
          @include custom(870) {
            font-size: 1.8rem;
            margin: 0 0 0.5rem 0;
          }
          @include custom(450) {
            font-size: 1.5rem;
            line-height: 100%;
            margin: 0 0 1rem 0;
          }
        }
        .text {
          @include F28-400;
          // max-width: 54rem;
          margin-bottom: 1.5rem;
          @include custom(1200) {
            font-size: 1.75rem;
            line-height: 100%;
          }
          @include custom(1050) {
            font-size: 1.5rem;
            line-height: 100%;
          }
          @include custom(530) {
            font-size: 1.1rem;
            line-height: 120%;
          }
        }
        .subtext {
          padding: 0 2rem;
          margin-bottom: 2rem;

          & li {
            &::before {
              content: "•";
              color: black;
              display: inline-block;
              width: 1em;
              margin-left: -2rem;
            }

            @include F32-600;
            font-size: 1.8rem;
            margin: 0 0 1rem 0;

            @include custom(1200) {
              line-height: 100%;
            }
            @include custom(530) {
              font-size: 1.6rem;
              line-height: 120%;
            }
            @include custom(450) {
              font-size: 1.5rem;
              line-height: 100%;
            }
          }
          & div {
            // max-width: 54rem;
            @include F28-400;
            font-size: 1.6rem;
            @include custom(1200) {
              line-height: 100%;
            }
            @include custom(530) {
              font-size: 1.1rem;
              line-height: 120%;
            }
          }
        }
        order: 1;
      }
      .image {
        margin: 30px auto;
        max-width: 40rem;
        max-height: 60rem;
        // @include custom(875) {
        //   display: none;
        // }
        & img {
          width: 100%;
          height: 100%;
        }
      }
      .app {
        @include custom(875) {
          display: none;
        }
      }
      .adaptive {
        display: none;
        @include custom(875) {
          display: block;
        }
      }
      @include custom(875) {
        display: flex;
        flex-direction: column;
      }
    }
  }
}
</style>
