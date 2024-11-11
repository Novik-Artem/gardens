<template>
  <div :class="$style.container">
    <div :class="$style.cards">
      <div :class="$style.card" v-for="card in items" :key="card.title">
        <div :class="$style.title">{{ card.title }}</div>
        <div :class="$style.text">{{ card.text }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          title: "Fund Garden Infrastructure",
          text: "Up to 1,000$ will cover construction materials, soil, seeds, and tools.",
        },
        {
          title: "Support Educational Resources",
          text: "Up to 1,000$ will fund teacher aids, workshop materials and lesson plans to help integrate the school curriculum into garden activities.",
        },
      ],
    };
  },
};
</script>

<style lang="scss" module>
.container {
  @include container;
  .cards {
    margin: -8rem 0 0 0;
    position: relative;
    z-index: 2;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 5.5rem;
    @include custom(970) {
      grid-template-columns: 1fr;
      gap: 2rem;
    }
    .card {
      background-color: $brown;
      padding: 3.125rem;
      border-radius: 1.25rem;
      .title {
        @include F36-500;
        margin: 0 0 1rem 0;
        @include custom(560) {
          font-size: 1.8rem;
          line-height: 100%;
        }
      }
      .text {
        @include F28-500;
        @include custom(560) {
          font-size: 1.5rem;
          line-height: 120%;
        }
      }
    }
  }
}
</style>
