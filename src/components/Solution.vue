<template>
  <div :class="$style.container">
    <div :class="$style.content">
      <div :class="$style.image">
        <img src="/images/solution/1.png" alt="" />
      </div>
      <div :class="$style.info">
        <div :class="$style.title">Our Solution</div>
        <div :class="$style.items">
          <div :class="$style.item">
            <div :class="$style.title">Start a school or community garden</div>
            <div :class="$style.text">
              Starting a school or community garden is a powerful way to bring
              people together, foster hands-on learning, and promote healthy
              living. These gardens serve as living classrooms that teach
              sustainable practices, connect individuals with nature, and
              inspire a sense of pride in growing and sharing fresh, nutritious
              food.
            </div>
          </div>
          <div :class="$style.item">
            <div :class="$style.title">Start a school or community garden</div>
            <div :class="$style.text">
              Starting a school or community garden is a powerful way to bring
              people together, foster hands-on learning, and promote healthy
              living. These gardens serve as living classrooms that teach
              sustainable practices, connect individuals with nature, and
              inspire a sense of pride in growing and sharing fresh, nutritious
              food.
            </div>
          </div>
          <div :class="$style.item">
            <div :class="$style.title">Start a school or community garden</div>
            <div :class="$style.text">
              Starting a school or community garden is a powerful way to bring
              people together, foster hands-on learning, and promote healthy
              living. These gardens serve as living classrooms that teach
              sustainable practices, connect individuals with nature, and
              inspire a sense of pride in growing and sharing fresh, nutritious
              food.
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" module>
.container {
  @include container;
  margin-bottom: 6.25rem;
  @include custom(720) {
    margin-bottom: 4rem;
  }
  .content {
    display: grid;
    grid-template-columns: 1fr 2fr;
    gap: 3.125rem;
    @include custom(720) {
      display: block;
    }
    .image {
      max-width: 26rem;
      max-height: 82rem;
      @include custom(940) {
        max-width: 15rem;
        max-height: 40rem;
      }
      @include custom(720) {
        display: none;
      }
      & img {
        width: 100%;
        height: 100%;
      }
    }
    .info {
      .title {
        @include F64-900;
        margin: 0 0 6.25rem 0;
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
      .items {
        .item {
          margin: 0 0 3.125rem 0;
          @include custom(1050) {
            margin: 0 0 2rem 0;
          }
          @include custom(800) {
            margin: 0 0 1.5rem 0;
          }
          &:last-child {
            margin: 0;
          }
          .title {
            @include F36-500;
            margin: 0 0 1.5rem 0;
            @include custom(1200) {
              font-size: 2rem;
              margin: 0 0 1rem 0;
            }
            @include custom(800) {
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
        }
      }
    }
  }
}
</style>
