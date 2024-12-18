<template>
  <div :class="$style.wrapper">
    <div :class="$style.container">
      <div :class="$style.title">What you need</div>
      <div :class="$style.text">
        There are many ways to garden: in-ground garden beds, raised rows,
        raised garden beds, straw bales, and container gardens
      </div>

      <div :class="$style.slider">
        <div @click="prev" :class="$style.button">
          <img src="/icons/arrow.svg" alt="" />
        </div>
        <div :class="$style.container">
          <div
            :class="$style.wrapper2"
            :style="{
              transform: `translateX(${-currentIndex * (100 / count)}%)`,
            }"
          >
            <img
              v-for="(image, index) in images"
              :key="index"
              :src="image.img"
              :class="$style.image"
            />
          </div>
        </div>
        <div @click="next" :class="($style.button, $style.next)">
          <img src="/icons/arrow.svg" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    if (window.innerWidth < 950) {
      this.count = 2;
    }
    if (window.innerWidth < 650) {
      this.count = 1;
    }
  },
  data() {
    return {
      currentIndex: 0,
      count: 3,
      images: [
        {
          img: "/images/slider/1.png",
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
          img: "/images/slider/8.png",
        },
      ],
    };
  },
  methods: {
    next() {
      if (this.currentIndex < this.images.length - this.count) {
        this.currentIndex++;
      }
    },
    prev() {
      if (this.currentIndex > 0) {
        this.currentIndex--;
      }
    },
  },
};
</script>

<style lang="scss" module>
.wrapper {
  background-color: $yellow;
  padding: 3rem 1rem;
  margin: 0 0 6.25rem 0;
  @include tablet {
    margin: 0 0 4rem 0;
  }
  .container {
    .title {
      @include F64-900;
      color: $white;
      text-align: center;
      margin: 0 0 1.5rem 0;
      @include custom(830) {
        font-size: 3rem;
        line-height: 100%;
      }
      @include mobile {
        font-size: 2.58rem;
      }
    }
    .text {
      @include F28-400;
      margin: 0 auto 3rem auto;
      max-width: 60rem;
      text-align: center;
      color: $white;
      @include custom(500) {
        line-height: 120%;
      }
    }
    .slider {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 1rem;
      .button {
        background-color: $white;
        border-radius: 50%;
        padding: 0.8rem;
        cursor: pointer;

        & img {
          width: 2rem;
          height: 2rem;
          transform: rotate(225deg);
          @include custom(420) {
            width: 1.2rem;
            height: 1.2rem;
          }
        }
      }
      .next {
        background-color: $white;
        border-radius: 50%;
        padding: 0.8rem;
        cursor: pointer;

        & img {
          width: 2rem;
          height: 2rem;
          transform: rotate(45deg);
          @include custom(420) {
            width: 1.2rem;
            height: 1.2rem;
          }
        }
      }

      .container {
        overflow: hidden;
        max-width: 998px;
        @include custom(940) {
          width: 500px;
        }
        @include custom(650) {
          width: 300px;
        }
        .wrapper2 {
          display: flex;
          align-items: center;
          transition: all 0.3s ease-in-out;

          .image {
            width: calc(100% / 3 - 11px);
            height: auto;
            margin-right: 11px;
            @include custom(940) {
              width: calc(100% / 2 - 11px);
            }
            @include custom(650) {
              width: 100%;
              margin-right: 0;
            }
            &:last-child {
              margin-right: 0;
            }
          }
        }
      }
    }
  }
}
</style>
