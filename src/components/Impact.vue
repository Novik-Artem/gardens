<template>
  <div :class="$style.wrapper">
    <div :class="$style.container">
      <div :class="$style.title">Our Impact</div>
      <div :class="$style.points">
        <div :class="$style.point" v-for="item in points" :key="item.title">
          <div :class="$style.subtitle">
            {{ item.title }}
          </div>
          <div :class="$style.text">
            {{ item.text }}
          </div>
        </div>
      </div>
    </div>
    <img src="/images/impact/1.png" alt="" :class="$style.image" />
    <img src="/images/impact/2.png" alt="" :class="$style.image2" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      points: [
        {
          title: "2022/23",
          text: "$11,000 awarded to 7 Schools with 665 Children",
        },
        {
          title: "2023/24",
          text: "$20,000 to 10 Schools with 1 444 Children",
        },
        {
          title: "2024/25",
          text: "$22,000 to 11 Schools with 3 723 Children",
        },
      ],
    };
  },
};
</script>

<style lang="scss" module>
.wrapper {
  background-color: $light-brown;
  padding: 3.215rem 0;
  position: relative;
  .container {
    @include container;

    .title {
      @include F64-900;
      text-align: center;
      margin: 0 0 3.125rem 0;
      @include custom(830) {
        font-size: 3rem;
        line-height: 100%;
      }
      @include custom(350) {
        font-size: 2.8rem;
      }
    }
    .points {
      .point {
        display: flex;
        gap: 6.25rem;
        border-bottom: 0.125rem solid $black;
        margin: 0 0 3.125rem 0;
        padding-bottom: 3.125rem;
        @include custom(1050) {
          gap: 3rem;
        }
        @include custom(890) {
          padding-bottom: 1rem;
        }
        @include custom(630) {
          gap: 1rem;
          margin: 0 0 1rem 0;
        }
        @include custom(530) {
          display: block;
        }
        &:last-child {
          border: none;
        }
        .subtitle {
          @include F76-400;
          @include custom(1010) {
            font-size: 4rem;
          }
          @include custom(890) {
            font-size: 3rem;
          }
          @include custom(690) {
            font-size: 2.4rem;
          }
          @include custom(630) {
            font-size: 2.2rem;
            line-height: 100%;
            margin: 0 0 1rem 0;
          }
        }
        .text {
          @include F36-400;
          @include custom(1010) {
            font-size: 2rem;
          }
          @include custom(890) {
            font-size: 1.5rem;
          }
          @include custom(690) {
            font-size: 1.4rem;
          }
          @include custom(630) {
            font-size: 1.2rem;
            line-height: 100%;
          }
        }
      }
    }
  }
  .image2 {
    position: absolute;
    top: 0;
    left: 0;
    width: 15rem;
    @include custom(530) {
      width: 10rem;
    }
    @include mobile {
      width: 6rem;
    }
  }
  .image {
    position: absolute;
    bottom: 0;
    right: 2rem;
    width: 15rem;
    @include custom(530) {
      width: 10rem;
    }
    @include mobile {
      width: 6rem;
    }
  }
}
</style>
