<template>
  <div :class="$style.container">
    <div :class="$style.top">
      <div :class="$style.left">
        <div :class="$style.text">
          <span>Application Period:</span> September 15- October 15, 2024
        </div>
        <div :class="$style.text">
          <span>Implementation Period:</span> January – June 2025
        </div>
      </div>
      <div :class="$style.right">
        <div :class="$style.title">Meet the Winners</div>
        <div :class="$style.links">
          <div v-for="link in links" :key="link.text">
            <a :href="link.file" download :class="$style.link">
              <div>{{ link.text }}</div>
              <img :src="link.icon" alt="" />
            </a>
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
      links: [
        {
          text: "2022",
          icon: "/icons/arrow.svg",
          file: "/files/22_Winners.pdf",
        },
        {
          text: "2023",
          icon: "/icons/arrow.svg",
          file: "/files/23_Winners.pdf",
        },
        {
          text: "2024",
          icon: "/icons/arrow.svg",
          file: "/files/24_Winners.pdf",
        },
      ],
    };
  },
};
</script>

<style lang="scss" module>
.container {
  @include container;
  margin-bottom: 3.125rem;
  .top {
    display: grid;
    grid-template-columns: 1fr 1fr;
    justify-content: space-between;
    align-items: center;
    gap: 1rem;
    @include custom(940) {
      grid-template-columns: 1fr;
    }
    .left {
      .text {
        @include F32-400;
        @include custom(1230) {
          font-size: 1.8rem;
          line-height: 100%;
        }
        @include custom(1100) {
          font-size: 1.5rem;
          line-height: 150%;
        }
        @include custom(550) {
          font-size: 1.2rem;
        }
        @include custom(385) {
          font-size: 1rem;
        }
        & span {
          font-weight: 600;
        }
      }
      @include custom(940) {
        margin: 0 0 2rem 0;
      }
    }
    .title {
      @include F32-600;
      margin: 0 0 2rem 0;
      @include custom(550) {
        font-size: 1.5rem;
      }
      @include custom(385) {
        font-size: 1.3rem;
      }
    }
    .links {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 1.5rem;
      .link {
        background-color: $light-brown;
        border-radius: 0.625rem;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        gap: 1rem;
        padding: 1rem;
        cursor: pointer;
        @include custom(550) {
          padding: 0.5rem;
          gap: 0.5rem;
        }
        & div {
          @include F32-600;
          @include custom(550) {
            font-size: 1.5rem;
          }
        }

        & img {
          width: 3rem;
          height: 3rem;
          @include custom(550) {
            width: 2rem;
            height: 2rem;
          }
        }
      }
    }
  }
}
</style>
