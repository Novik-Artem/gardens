<template>
  <div :class="$style.container">
    <div :class="$style.title">Our Solutions</div>
    <div :class="$style.content">
      <div :class="$style.column">
        <div :class="$style.item">
          <div :class="$style.subtitle">
            1. Start a school or community garden
          </div>
          <div :class="$style.text">
            Starting a school or community garden is a powerful way to bring
            people together, foster hands-on learning, and promote healthy
            living. These gardens serve as living classrooms that teach
            sustainable practices, connect individuals with nature, and inspire
            a sense of pride in growing and sharing fresh, nutritious food.
          </div>
          <div :class="$style.subtext">
            <li>Grant Opportunities</li>
            <div>
              As funds become available, ResiliencyGardens.org provides support
              for school and community garden infrastructure, covering expenses
              for construction materials, soil, seeds, and tools, as well as
              educational resources, including instructors and workshops. We
              invite you to explore our grant programs below to find the one
              that best suits your needs.
            </div>
          </div>
          <div :class="$style.subtext">
            <li>Inclusive Educational Gardens in Polish Schools 2025s</li>
            <div>
              ResiliencyGardens.org and Seed Programs International are working
              together to offer support to Polish schools for environmental
              education and to aid in the integration of special needs children,
              including Ukrainian refugees and other non-native students into
              their school communities. Ten schools will each be awarded up to
              $2,000 in funding for their school garden programs.
            </div>
          </div>
        </div>
        <Applicate :class="$style.app" />
      </div>
      <div :class="$style.column">
        <div :class="$style.item">
          <div :class="$style.subtitle">
            2. Start a school or community garden
          </div>
          <div :class="$style.text">
            Anyone can grow vegetables and everyone enjoys watching a seed they
            planted sprout and grow. Whether on a windowsill, a balcony or in a
            garden bed, we can all make a difference
          </div>
        </div>
        <div :class="$style.image">
          <img src="/images/solution/1.png" alt="" />
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
  margin-bottom: 6.25rem;
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
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
    justify-content: space-between;
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
          max-width: 54rem;
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
            max-width: 54rem;
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
      }
      .image {
        margin: 0 auto;
        max-width: 24rem;
        max-height: 60rem;
        @include custom(875) {
          display: none;
        }
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
    }
  }
}
</style>
