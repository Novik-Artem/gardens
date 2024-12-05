<template>
  <div :class="$style.container">
    <div :class="$style.title">
      <p>Resiliency</p>
      <p>Gardens</p>
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
      padding: 4rem 0 0 0;
    }
    @include custom(375) {
      font-size: 4rem;
      padding: 3rem 0 0 0;
      margin-bottom: 2rem;
    }
  }
}
</style>
