<template>
  <div :class="$style.container">
    <div :class="$style.content">
      <div :class="$style.left">
        <div :class="$style.title">Contact us</div>
        <div :class="$style.text">
          To learn more, please contact June Lavelle at
          <a href="mailto:june.lavelle@gmail.com">june.lavelle@gmail.com</a>.
        </div>
      </div>
      <div :class="$style.right">
        <div :class="$style.image">
          <img src="/images/contacts/1.png" alt="" />
        </div>
        <div :class="$style.text">
          <div>June Lavelle</div>
          <span>Project founder</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" module>
.container {
  @include container;
  margin-bottom: 6.25rem;
  @include tablet {
    margin-bottom: 4rem;
  }
  .content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 19.5rem;
    align-items: center;
    @include custom(1030) {
      gap: 2rem;
    }
    @include custom(800) {
      grid-template-columns: 1fr;
    }
    .title {
      @include F64-500;
      margin: 0 0 2.5rem 0;
    }
    .text {
      @include F36-400;
      font-size: 1.5rem;
      & a {
        text-decoration: underline;
      }
      @include custom(370) {
        font-size: 1.2rem;
        line-height: 120%;
      }
    }
    .right {
      .text {
        text-align: center;
        & div {
          @include F64-400;
        }
        & span {
          @include F20-400;
        }
      }
      .image {
        max-width: 26rem;
        max-height: 26rem;
        margin: 0 auto;
        & img {
          width: 100%;
          height: 100%;
        }
      }
    }
  }
}
</style>
