<template>
  <div :class="$style.wrapper">
    <div :class="$style.container">
      <div :class="$style.title">{{ $t("mattersSection.title") }}</div>
      <p :class="$style.text">
        {{ $t("mattersSection.firstText") }}
      </p>
      <p :class="$style.text">
        {{ $t("mattersSection.secondText") }}
      </p>
    </div>
  </div>
</template>

<style lang="scss" module>
.wrapper {
  background-color: $blue;
  margin: 0 0 6.25rem 0;
  @include custom(720) {
    margin: 0 0 4rem 0;
  }
  .container {
    @include container;
    margin-top: -18rem;
    padding-top: 24rem;
    padding-bottom: 4rem;
    @include custom(800) {
      margin-top: -10rem;
      padding-top: 12rem;
    }
    @include mobile {
      margin-top: 0;
      padding-top: 2rem;
      padding-bottom: 2rem;
    }
    .title {
      @include F64-900;
      text-align: center;
      color: $white;
      margin: 0 0 3rem 0;
      @include custom(830) {
        font-size: 3rem;
        line-height: 100%;
      }
      @include mobile {
        font-size: 2.8rem;
      }
    }
    .text {
      @include F36-400;
      color: $white;
      margin: 0 0 2rem 0;
      &:last-child {
        margin: 0;
      }
      @include custom(830) {
        font-size: 1.5rem;
        line-height: 120%;
      }
      @include mobile {
        font-size: 1.2rem;
      }
    }
  }
}
</style>
