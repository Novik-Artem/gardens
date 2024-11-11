<template>
  <div :class="$style.wrapper">
    <div :class="$style.container">
      <div :class="$style.title">Support Environmental Education</div>
      <div :class="$style.subtitle">Help Build School Gardens</div>
      <div :class="$style.cards">
        <div :class="$style.card" v-for="card in cards" :key="card.link">
          <div :class="$style.left">
            <div :class="$style.cardTitle">{{ card.title }}</div>
            <div :class="$style.link">
              {{ card.link }}
              <img src="/icons/gold-arrow.svg" alt="" />
            </div>
          </div>
          <div :class="$style.right">
            {{ card.text }}
          </div>
        </div>
      </div>
    </div>
    <img src="/images/support/1.png" alt="" :class="$style.firstImage" />
    <img src="/images/support/2.png" alt="" :class="$style.secondImage" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          title: "Promote Environmental Stewardship",
          link: "Start Team Gardening",
          text: "Through hands-on learning, students will gain direct experience with nature, learning about ecosystems, plant life cycles, and the importance of biodiversity. Activities like composting, recycling, and water conservation will encourage sustainable habits that will positively impact their communities.",
        },
        {
          title: "Promote Teamwork and Collaboration",
          link: "Grow Together",
          text: "By planning and maintaining the garden together, students will develop collaboration and problem-solving skills in a safe, welcoming space that fosters teamwork and a sense of belonging for all, including students with special needs.",
        },
        {
          title: "Encourage Healthy Living",
          link: "Learn to Grow",
          text: "Students will spend time outdoors, planting fruits and vegetables, learning about the benefits of locally grown food for both the environment and personal health.",
        },
      ],
    };
  },
};
</script>

<style lang="scss" module>
.wrapper {
  background-color: $light-green;
  position: relative;
  padding: 5.625rem 0 13.5rem 0;
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
        font-size: 2rem;
        margin: 0 0 1rem 0;
        line-height: 100%;
      }
    }
    .subtitle {
      @include F48-400;
      text-align: center;
      margin: 0 0 3rem 0;
      @include custom(750) {
        font-size: 2rem;
        line-height: 100%;
      }
    }
    .cards {
      display: grid;
      grid-template-columns: 1fr;
      gap: 1.875rem;
      position: relative;
      z-index: 2;
      .card {
        background-color: $white;
        padding: 2.5rem;
        border-radius: 1.25rem;
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 1rem;
        position: relative;
        @include custom(1040) {
          grid-template-columns: 1fr;
        }
        @include custom(560) {
          padding: 1rem;
        }
        .left {
          @include custom(1040) {
            order: 1;
          }
        }
        .cardTitle {
          @include F36-600;
          margin: 0 0 6.25rem 0;
          @include custom(1040) {
            margin: 0 0 1rem 0;
          }
          @include custom(560) {
            margin: 0;
            font-size: 1.8rem;
            line-height: 100%;
          }
          @include custom(380) {
            font-size: 1.5rem;
          }
        }
        .link {
          cursor: pointer;
          @include F28-600;
          border: 0.1875rem solid $brown;
          border-radius: 0.625rem;
          padding: 1.625rem 1.25rem;
          display: inline-flex;
          align-items: center;
          gap: 1rem;
          @include custom(1040) {
            position: absolute;
            bottom: 2.5rem;
            left: 2.5rem;
          }
          @include custom(560) {
            font-size: 1.5rem;
            padding: 1rem;
            left: 1rem;
            bottom: 1rem;
          }
          @include custom(370) {
            font-size: 1.2rem;
          }
        }
        .right {
          @include F32-500;
          @include custom(1250) {
            font-size: 1.8rem;
          }
          @include custom(1040) {
            order: 2;
            margin: 0 0 10rem 0;
          }
          @include custom(560) {
            font-size: 1.5rem;
            margin: 0 0 7rem 0;
          }
        }
      }
    }
  }
  .firstImage {
    position: absolute;
    top: 5.375rem;
    left: 5.375rem;
    @include custom(1400) {
      display: none;
    }
  }
  .secondImage {
    position: absolute;
    bottom: 10rem;
    right: 2rem;
    width: 15rem;
    height: 10rem;
    @include custom(1400) {
      display: none;
    }
  }
}
</style>
