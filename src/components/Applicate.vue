<template>
  <div :class="$style.content">
    <div :class="$style.title" id="winners">
      {{ $t("solutionSection.first.winners") }}
    </div>
    <div :class="$style.cta">
      <div :class="$style.links">
        <div v-for="link in links" :key="link.text">
          <a :href="link.file" target="_blank" :class="$style.link">
            <div>{{ link.text }}</div>
            <img :src="link.icon" alt="" />
          </a>
        </div>
      </div>
      <a
        href="https://secure.givelively.org/donate/resiliencygardensorg"
        :class="$style.button"
        target="_blank"
      >
        Donate now
      </a>
      <div :class="$style.donate">
        {{ $t("solutionSection.first.donate") }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          text: "2022",
          icon: "/icons/arrow.svg",
          file: "/files/22_Winners.pdf",
        },
        {
          text: "2023",
          icon: "/icons/arrow.svg",
          file: "/files/23_Winners.pdf",
        },
        {
          text: "2024",
          icon: "/icons/arrow.svg",
          file: "/files/24_Winners.pdf",
        },
      ],
    };
  },
};
</script>

<style lang="scss" module>
.title {
  @include F32-600;
  margin: 0 0 2rem 0;
  @include custom(550) {
    font-size: 1.5rem;
  }
  @include custom(385) {
    font-size: 1.3rem;
  }
}
.links {
  max-width: 31.25rem;
  margin-bottom: 3rem;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 1.5rem;
  @include custom(500) {
    margin-bottom: 1.5rem;
  }
  .link {
    background-color: $light-brown;
    border-radius: 0.625rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    gap: 1rem;
    padding: 1rem;
    cursor: pointer;
    @include custom(550) {
      padding: 0.5rem;
      gap: 0.5rem;
    }
    & div {
      @include F32-600;
      @include custom(550) {
        font-size: 1.5rem;
      }
    }

    & img {
      width: 3rem;
      height: 3rem;
      @include custom(550) {
        width: 2rem;
        height: 2rem;
      }
    }
  }
}
.text {
  @include F32-400;
  @include custom(1230) {
    font-size: 1.8rem;
    line-height: 100%;
  }
  @include custom(1100) {
    font-size: 1.5rem;
    line-height: 150%;
  }
  @include custom(550) {
    font-size: 1.2rem;
  }
  @include custom(385) {
    font-size: 1rem;
  }
  & span {
    font-weight: 600;
  }
}
.button {
  margin: 5rem auto 1.25rem auto;
  @include F32-600;
  padding: 1.25rem 1.875rem;
  border: 0.3125rem solid $orange;
  border-radius: 0.625rem;
  background-color: $white;
  font-weight: 500;
  cursor: pointer;
  display: flex;
  justify-content: center;
  transition: all 0.3s ease-in-out;
  &:hover {
    background-color: $orange;
    color: $white;
  }
  @include custom(500) {
    margin-top: 1.5rem;
  }
}
.donate {
  @include F28-400;
  text-align: center;
  @include custom(425) {
    font-size: 1.2rem;
  }
}
</style>
