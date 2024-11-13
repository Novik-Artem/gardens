<template>
  <div :class="$style.wrapper">
    <div :class="$style.container">
      <div :class="$style.title">Where to start?</div>
      <div :class="$style.text">
        If you’ve no land, it doesn’t mean you can’t garden.
      </div>
      <div :class="$style.text">A garden has four basic needs:</div>
    </div>
    <img src="/images/start/1.png" alt="" :class="$style.image" />
    <img src="/images/start/2.png" alt="" :class="$style.image2" />
    <img src="/images/start/3.png" alt="" :class="$style.image3" />
    <img src="/images/start/4.png" alt="" :class="$style.image4" />
    <img src="/images/start/5.png" alt="" :class="$style.image5" />
  </div>
</template>

<style lang="scss" module>
.wrapper {
  background-color: $orange;
  position: relative;
  .container {
    max-width: 72rem;
    margin: 0 auto;
    padding: 6.25rem 1rem;
    @include custom(580) {
      padding: 3rem 1rem;
    }
    .title {
      text-align: center;
      @include F112-900;
      color: $white;
      margin: 0 0 3.75rem 0;
      @include custom(970) {
        font-size: 5rem;
        margin: 0 0 2rem 0;
      }
      @include custom(580) {
        font-size: 3rem;
        margin: 0 0 1rem 0;
        line-height: 50%;
      }
      @include custom(350) {
        font-size: 2.5rem;
      }
    }
    .text {
      @include F28-400;
      color: $white;
      max-width: 58rem;
      text-align: center;
      margin: 0 auto 4rem auto;
      @include custom(970) {
        font-size: 1.5rem;
        margin: 0 auto 2.2rem auto;
        line-height: 100%;
      }
      @include custom(580) {
        margin: 0;
        line-height: 130%;
        text-align: center;
      }
      &:last-child {
        margin: 0 auto;
      }
    }
  }
  .image {
    position: absolute;
    top: 5.625rem;
    left: 5.625rem;
    @include custom(1325) {
      width: 5rem;
      height: 8rem;
    }
    @include custom(1080) {
      width: 4rem;
      height: 7rem;
      left: 1rem;
      top: 1rem;
    }
    @include custom(750) {
      display: none;
    }
  }
  .image2 {
    position: absolute;
    bottom: -11rem;
    left: 13.125rem;
    @include custom(1325) {
      width: 12rem;
      height: 16rem;
      bottom: 2rem;
      left: 6rem;
    }
    @include custom(1080) {
      width: 8rem;
      height: 11rem;
      left: 2rem;
      bottom: 2rem;
    }
    @include custom(750) {
      display: none;
    }
  }
  .image3 {
    position: absolute;
    bottom: -6rem;
    right: 40rem;
    @include custom(1325) {
      width: 6rem;
      height: 10rem;
      bottom: 2rem;
      left: 24rem;
    }
    @include custom(1200) {
      display: none;
    }
  }
  .image4 {
    position: absolute;
    bottom: -8rem;
    right: 24rem;
    @include custom(1325) {
      width: 8rem;
      height: 10rem;
      bottom: 4rem;
      right: 8rem;
    }
    @include custom(1080) {
      width: 8rem;
      height: 11rem;
      right: 2rem;
      bottom: 2rem;
    }
    @include custom(750) {
      display: none;
    }
  }
  .image5 {
    position: absolute;
    top: 3.875rem;
    right: 4.5625rem;
    @include custom(1325) {
      width: 6rem;
      height: 10rem;
    }
    @include custom(1080) {
      width: 6rem;
      height: 9rem;
      right: 2rem;
      top: 2rem;
    }
    @include custom(750) {
      display: none;
    }
  }
}
</style>
