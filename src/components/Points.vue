<template>
  <div :class="$style.wrapper">
    <div :class="$style.container">
      <div :class="$style.points">
        <div :class="$style.list">
          <div v-for="item in points" :key="item.title" :class="$style.li">
            <span :class="$style.title" :style="{ color: item.color }">
              {{ item.title }}
            </span>
            <span>{{ item.text }}</span>
          </div>
        </div>
        <div :class="$style.image">
          <img src="/images/points/2.png" alt="" />
        </div>
      </div>
    </div>
    <Slider />
    <div :class="$style.container">
      <div :class="$style.points">
        <div :class="$style.list">
          <div :class="$style.li">
            <div :class="$style.purple">
              People who have access to their own vegetable garden
              <span>consume 40% more</span> fresh vegetables and herbs and,
              consequently, eat less junk food.
            </div>
          </div>
          <div :class="$style.li">
            <div :class="$style.orange">
              Vegetables and herbs lose 30-50% of their useful properties within
              <span>5-10 days.</span> Local vegetable gardens allow you to eat
              vegetables and herbs <span>immediately after harvesting.</span>
            </div>
          </div>
          <div :class="$style.li">
            <div :class="$style.green">
              Working on a garden has a positive effect on personal
              <span> well-being</span>
              and gardening with others enhances
              <span>social connections.</span>
            </div>
          </div>
        </div>
        <div :class="$style.image">
          <img src="/images/points/1.svg" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Slider from "./Slider.vue";
export default {
  components: {
    Slider,
  },
  data() {
    return {
      points: [
        {
          title: "Soil.",
          text: " Great soil is essential to growing vegetables, fruits, and other plant life.",
          color: "#ff7235",
        },
        {
          title: "Sun.",
          text: " Most vegetables need at least 6 hours of unobstructed sun or artificial light per day, although some crops, such as broccoli, lettuce, spinach, and other greens, can tolerate less.",
          color: "#ffbe21",
        },
        {
          title: "Water.",
          text: " Plants need water to gather nutrients from the soil.",
          color: "#30b9e2",
        },
        {
          title: "Seeds.",
          text: " Source and buy quality seeds locally that are suitable for our climate and your type of garden.",
          color: "#4a9b52",
        },
      ],
    };
  },
};
</script>

<style lang="scss" module>
.wrapper {
  .container {
    @include container;
    .points {
      display: grid;
      grid-template-columns: 1fr 1fr;
      align-items: end;
      gap: 1rem;
      margin: 0 0 6.25rem 0;
      @include tablet {
        grid-template-columns: 1fr;
        margin: 0 0 4rem 0;
      }
      .list {
        @include tablet {
          order: 2;
        }
        .li {
          margin: 0 0 1.25rem 0;
          @include F32-500;
          @include custom(1100) {
            font-size: 1.5rem;
            line-height: 120%;
          }
          @include custom(870) {
            font-size: 1.35rem;
          }
          @include custom(530) {
            font-size: 1.1rem;
          }
          &:last-child {
            margin: 0;
          }
        }
        .purple {
          & span {
            color: $purple;
          }
        }
        .orange {
          & span {
            color: $orange;
          }
        }
        .green {
          & span {
            color: $green;
          }
        }
      }
      .image {
        max-width: 50rem;
        max-height: 50rem;
        & img {
          width: 100%;
          height: 100%;
        }
        @include tablet {
          order: 1;
          margin: 0 0 2rem 0;
        }
      }
    }
  }
}
</style>
