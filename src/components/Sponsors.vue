<template>
  <div :class="$style.container">
    <div :class="$style.title">{{ $t("sponsorsSection.title") }}</div>
    <div :class="$style.logo">
      <img :src="$t('sponsorsSection.cardImage')" alt="" />
    </div>
    <div :class="$style.text">
      {{ $t("sponsorsSection.cardText") }}
    </div>
  </div>
</template>

<style lang="scss" module>
.container {
  max-width: 50rem;
  margin: 8rem auto;
  padding: 3rem;
  border: 2px solid $orange;
  border-radius: 1.625rem;
  color: $black;
  .title {
    @include F64-900;
    text-align: center;
    margin: 0 0 3rem 0;
    @include custom(1080) {
      font-size: 3rem;
    }
    @include custom(750) {
      font-size: 2rem;
      line-height: 100%;
    }
  }
  .logo {
    display: flex;
    justify-content: center;
    margin: 0 0 3rem 0;

    & img {
      border-radius: 1.625rem;
      @include custom(540) {
        width: 8rem;
        height: 8rem;
      }
    }
  }
  .text {
    text-align: center;
    font-size: 1.3rem;
    line-height: 100%;
  }
}
</style>
