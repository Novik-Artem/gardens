<template>
  <div :class="$style.wrapper">
    <div :class="$style.container">
      <div :class="$style.points">
        <div :class="$style.list">
          <div :class="$style.li">
            <div :class="$style.purple">
              {{ $t("solutionSection.second.firstText") }}
            </div>
          </div>
          <div :class="$style.li">
            <div :class="$style.orange">
              {{ $t("solutionSection.second.secondText") }}
            </div>
          </div>
          <div :class="$style.li">
            <div :class="$style.green">
              {{ $t("solutionSection.second.thirdText") }}
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

<style lang="scss" module>
.wrapper {
  @include custom(1325) {
    margin: 5rem 0 0 0;
  }
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
