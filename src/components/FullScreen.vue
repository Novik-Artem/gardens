<template>
  <div :class="$style.container">
    <div :class="$style.title">
      <p>Resiliency</p>
      <p>Gardens</p>
    </div>
    <div :class="$style.subtitle">Test subtitle that is centred</div>
    <div :class="$style.button">
      <a href="">Donate now</a>
    </div>
  </div>
</template>

<style lang="scss" module>
.container {
  height: 100vh;
  width: 100vw;
  background-repeat: no-repeat;
  background-size: cover;
  background-image: url("../assets/images/fullscreen.jpg");
  margin: 0 0 3.125rem 0;
  @include mobile {
    margin: 0 0 1.5rem 0;
  }
  .title {
    padding: 6.25rem 0 0 0;
    @include F105-900;
    color: $white;
    text-align: center;
    margin-bottom: 3.25rem;
    @include custom(500) {
      font-size: 5rem;
      line-height: 100%;
    }
    @include custom(375) {
      font-size: 4rem;
      padding: 8rem 0 0 0;
      margin-bottom: 2rem;
    }
  }
  .subtitle {
    @include F36-600;
    text-align: center;
    color: $white;
    margin: 0 0 4rem 0;
    @include custom(440) {
      font-size: 1.8rem;
    }
    @include custom(340) {
      font-size: 1.6rem;
    }
  }
  .button {
    @include F36-600;
    color: $white;
    text-align: center;
    & a {
      padding: 1.5rem 3rem;
      background-color: $black;
      border-radius: 0.625rem;
      transition: all 0.5s ease-in-out;
      &:hover {
        background-color: $white;
        color: $black;
      }
    }
  }
}
</style>
