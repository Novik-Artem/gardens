<template>
  <div :class="$style.container">
    <div :class="$style.row">
      <div :class="$style.text">
        <div :class="$style.title">About us</div>
        <div :class="$style.subtext">
          ResiliencyGardens.org is a charitable organization dedicated to
          educating future generations by investing in school and community
          gardens that showcase sustainable agricultural practices, promote
          healthy living, and foster environmental stewardship.
        </div>
      </div>
      <div :class="$style.image">
        <img src="/images/about/1.png" alt="" />
      </div>
    </div>
    <div :class="$style.row">
      <div :class="$style.image">
        <img src="/images/about/2.png" alt="" />
      </div>
      <div :class="$style.text">
        <div :class="$style.title">Our goal</div>
        <div :class="$style.subtext">
          To create dynamic, hands-on learning environments that deepen our
          understanding of ecological processes, while inspiring people of all
          ages to experience the joy of growing and eating their own food.
        </div>
      </div>
    </div>
    <div :class="$style.row">
      <div :class="$style.text">
        <div :class="$style.title">Our vision</div>
        <div :class="$style.subtext">
          A world where communities are resilient, self-sufficient, and actively
          engaged in sustainable food systems that foster personal well-being
          and contribute to the health of our planet.
        </div>
      </div>
      <div :class="$style.image">
        <img src="/images/about/3.svg" alt="" />
      </div>
    </div>
  </div>
</template>

<style lang="scss" module>
.container {
  @include container;
  .row {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 3rem;
    @include custom(800) {
      margin: 0 0 5rem 0;
    }
    @include custom(530) {
      margin: 0 0 4rem 0;
      gap: 1.5rem;
    }
    @include custom(375) {
      margin: 0 0 2rem 0;
    }
    @include mobile {
      flex-direction: column;
      gap: 0;
    }
    &:nth-child(2) {
      @include custom(800) {
        margin: 0 0 10rem 0;
      }
      @include custom(530) {
        margin: 0 0 6rem 0;
      }
      @include mobile {
        margin: 0 0 4rem 0;
      }
      @include custom(375) {
        margin: 0 0 2rem 0;
      }
      .image {
        @include mobile {
          order: 1;
          margin: 0 0 4rem 0;
        }
      }
    }
    .text {
      .title {
        @include F64-900;
        margin: 0 0 2.25rem 0;
        @include custom(1000) {
          font-size: 2.5rem;
          margin: 0 0 0 0;
        }
        @include custom(530) {
          font-size: 2rem;
        }
      }
      .subtext {
        max-width: 45rem;
        @include F28-400;
        @include custom(1000) {
          font-size: 1.5rem;
          line-height: 100%;
        }
        @include custom(530) {
          font-size: 1.1rem;
          line-height: 120%;
        }
      }
      @include mobile {
        order: 2;
      }
    }
    .image {
      max-width: 26rem;
      max-height: 32rem;
      @include custom(800) {
        max-width: 14rem;
        max-height: 16rem;
      }
      @include mobile {
        order: 1;
        margin: 0 0 2rem 0;
      }
      & img {
        width: 100%;
        height: 100%;
      }
    }
    &:last-child {
      position: relative;
      display: flex;
      justify-content: center;
      @include custom(800) {
        justify-content: flex-end;
        margin: 0;
      }
      @include mobile {
        flex-direction: row;
        justify-content: flex-end;
        margin: 0 0 2rem 0;
      }
      @include custom(380) {
        display: block;
      }
      .text {
        position: absolute;
        top: 7rem;
        left: 0;

        @include custom(1000) {
          top: 9rem;
        }
        @include custom(900) {
          max-width: 38rem;
          top: 7rem;
        }
        @include custom(850) {
          max-width: 32rem;
          top: 5rem;
        }
        @include custom(800) {
          max-width: 32rem;
          top: -1rem;
        }
        @include custom(780) {
          max-width: 36rem;
        }
        @include custom(700) {
          max-width: 30rem;
        }
        @include custom(610) {
          max-width: 24rem;
          top: -3rem;
        }
        @include custom(530) {
          max-width: 20rem;
          top: 0;
        }
        @include mobile {
          top: 2rem;
        }
        @include custom(410) {
          top: 0;
        }

        @include custom(380) {
          position: static;
        }
      }
      .image {
        max-width: 100%;
        max-height: 100%;
        @include custom(800) {
          max-width: 34rem;
        }
        @include mobile {
          max-width: 24rem;
          margin: 5rem 0 0 0;
        }
        @include custom(410) {
          max-width: 18rem;
        }
        @include custom(380) {
          display: none;
        }
        & img {
          width: 100%;
          height: 100%;
        }
      }
    }
  }
}
</style>
