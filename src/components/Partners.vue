<template>
  <div :class="$style.container">
    <div :class="$style.title">Our Partners</div>
    <div :class="$style.subtitle">
      A heartfelt thanks to our partners for their dedication and contributions
      to the Resiliency Garden’s School and Community Gardens program
    </div>
    <div :class="$style.cards">
      <div :class="$style.card" v-for="card in cards" :key="card.image">
        <div
          :class="[$style.image, card.type ? $style.vertical : '']"
          v-if="card.image"
        >
          <img :src="card.image" alt="" />
        </div>
        <a :href="card.file" download :class="card.link ? $style.orange : ''">
          <div :class="$style.text">
            {{ card.text }}
          </div>
          <div :class="$style.link" v-if="card.link">
            {{ card.link }}
            <img src="/icons/arrow-white.svg" alt="" />
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          type: "vertical",
          image: "/images/partners/5.png",
          text: "Trips Beyond the Classroom offers Innovative Education that creates lifetime and generational impact by raising global awareness among youth to inspire future leaders. Safe challenges through travel, homestays, community service and virtual collaboration provide real-world experience, motivating students and teachers to go beyond the classroom! A special Beyond the Garden program has been designed to support educational institutions in creating young environmental stewards through gardening.",
        },
        {
          type: "vertical",
          image: "/images/partners/1.png",
          text: "Rybnik, in southern Poland, leads in sustainable food practices. The city created the Sustainable Public Meal Toolkit to promote plant-based diets among youth. Through the StratKIT+ project, Rybnik matched 10% of Resiliency Gardens grants, improving school garden infrastructure. In 2024, 1,484 students from nine schools participated in gardening, enhancing community engagement and integrating sustainable food systems into education.",
        },
        {
          image: "/images/partners/4.png",
          text: "Seed Programs International provides good quality seed, expertise, and training materials to humanitarian organizations working around the world to alleviate hunger and poverty. SPI’s in-kind grants are enabling schools, universities, foster homes and community organizations to establish edible gardens for learning and sharing.",
        },
        {
          image: "/images/partners/2.png",
          text: "Fundacja Naturalnego Rozwoju is dedicated to the holistic development of children and youth, with a special emphasis on ecological education and fostering connections with nature. Our mission is to nurture a generation of young individuals who are not only environmentally responsible but also actively engaged in their communities.",
        },
        {
          image: "/images/partners/3.png",
          text: "KidsGardening.org creates opportunities for kids to play, learn, and grow through gardening, engaging their natural curiosity and wonder. KG’s in-kind donation of Learning Tools for educators, parents and child caregivers are now available in Polish and Ukrainian.",
        },
        {
          text: "Join us in growing a healththier, more sustainable future",
          link: "Become a Corporate Sponsor",
          file: "/files/Corporate-appeal.pdf",
        },
      ],
    };
  },
};
</script>

<style lang="scss" module>
.container {
  @include container;
  margin-top: 6.25rem;
  margin-bottom: 6.25rem;
  @include tablet {
    margin-top: 4rem;
    margin-bottom: 4rem;
  }
  .title {
    @include F64-900;
    text-align: center;
    margin: 0 0 2rem 0;
    @include custom(1080) {
      font-size: 3rem;
    }
    @include custom(750) {
      font-size: 2rem;
      margin: 0 0 1rem 0;
      line-height: 100%;
    }
  }
  .subtitle {
    @include F36-500;
    text-align: center;
    margin: 0 0 3rem 0;
    @include custom(1130) {
      font-size: 1.8rem;
      line-height: 100%;
    }
    @include custom(1130) {
      margin: 0 0 2rem 0;
      font-size: 1.5rem;
    }
  }
  .cards {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4.8rem;
    @include custom(1050) {
      grid-template-columns: 1fr;
      gap: 2rem;
    }
    .card {
      .text {
        @include F28-400;
        @include custom(560) {
          font-size: 1.5rem;
          line-height: 100%;
        }
      }
      .image {
        @include custom(460) {
          max-width: 20rem;
          max-height: 20rem;
          margin: 0 auto 1.5rem auto;
          & img {
            width: 100%;
            height: 100%;
          }
        }
        &.vertical {
          @include custom(460) {
            max-width: 10rem;
            max-height: 10rem;
            margin: 0 auto 1.5rem auto;
            & img {
              width: 100%;
              height: 100%;
            }
          }
        }
      }
      .orange {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        height: 100%;
        background-color: $orange;
        border-radius: 1.625rem;
        padding: 1.5rem;
        .text {
          color: $white;
          @include F28-400;
          @include custom(560) {
            font-size: 1.5rem;
            line-height: 100%;
            margin: 0 0 3rem 0;
          }
          @include custom(500) {
            font-size: 1.3rem;
          }
        }
        .link {
          cursor: pointer;
          color: $white;
          display: flex;
          align-items: center;
          @include F28-400;
          @include custom(560) {
            font-size: 1.5rem;
            line-height: 100%;
          }
          @include custom(410) {
            font-size: 1.3rem;
          }
        }
      }
    }
  }
}
</style>
