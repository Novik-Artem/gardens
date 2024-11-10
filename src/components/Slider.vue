<template>
  <div :class="$style.wrapper">
    <div :class="$style.container">
      <div :class="$style.title">What you need</div>
      <div :class="$style.text">
        There are many ways to garden: in-ground garden beds, raised rows,
        raised garden beds, straw bales, and container gardens
      </div>
      <div :class="$style.slider">
        <div :class="$style.slide" v-for="item in slides" :key="item.img">
          <div :class="$style.image">
            <img :src="item.img" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slides: [
        {
          img: "/images/slider/test.png",
        },
        {
          img: "/images/slider/2.png",
        },
        {
          img: "/images/slider/3.png",
        },
        {
          img: "/images/slider/4.png",
        },
        {
          img: "/images/slider/5.png",
        },
        {
          img: "/images/slider/6.png",
        },
        {
          img: "/images/slider/7.png",
        },
        {
          img: "/images/slider/8.png",
        },
        {
          img: "/images/slider/9.png",
        },
        {
          img: "/images/slider/10.png",
        },
      ],
    };
  },
};
</script>

<style lang="scss" module>
@import "@/assets/styles/common.scss";

.wrapper {
  background-color: $yellow;
  padding: 3rem 1rem;
  .container {
    @include container;
    .title {
      @include F64-900;
      color: $white;
      text-align: center;
      margin: 0 0 3rem 0;
      @include custom(830) {
        font-size: 3rem;
        line-height: 100%;
      }
      @include mobile {
        font-size: 2.58rem;
      }
    }
    .text {
      @include F20-400;
      margin: 0 auto 2rem auto;
      max-width: 50rem;
      text-align: center;
      color: $white;
      @include custom(500) {
        line-height: 120%;
      }
    }
    .slider {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      min-width: 100%;
      overflow-x: auto;
      @include scrollbarX;
      padding-bottom: 0.5rem;

      .slide {
        white-space: nowrap;

        .image {
          width: 25rem;
          height: 36rem;
          @include custom(500) {
            width: 21rem;
            height: 32rem;
          }
          & img {
            width: 100%;
            height: 100%;
          }
        }
      }
    }
  }
}
</style>
