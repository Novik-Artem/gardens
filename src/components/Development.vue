<template>
  <div :class="$style.wrapper">
    <div :class="$style.container">
      <div :class="$style.title">Gardening helps a child’s development</div>
      <div :class="$style.content">
        <div :class="$style.column" v-for="item in cards" :key="item.title">
          <div :class="$style.subtitle">{{ item.title }}</div>
          <div :class="$style.text">{{ item.text }}</div>
        </div>
      </div>
      <div :class="$style.video">
        <iframe
          src="https://www.youtube.com/embed/IEfkdVHzyIo?si=UoB6LcOvTLgmdLhz"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin"
          allowfullscreen
        ></iframe>
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
          title: "Sensory development",
          text: "A garden is a place of wonder for a child. Children are absorbed by the textures, shapes, colors and scents of living plants and thrilled when they can enjoy their taste.  Gardening helps kids develop hand-eye coordination and build physical strength and important motor skills, such as cutting, planting, and writing.",
        },
        {
          title: "Intellectual skills",
          text: "Gardening involves planning, a skill that everyone needs. Kids should be included in this process. Support them in learning how to prepare the soil, plant, water, and weed.  They can report on what they have done already and what they think they should do next. In time, they will be able to identify the differences and characteristics of roots, stems, flowers, leaves, seeds and fruits. Gardening is a fun way to help kids learn something useful!",
        },
        {
          title: "Social skills",
          text: "Kids learn to cooperate by working together to nurture and care for their plants. They can paint flowerpots together and share their knowledge of different plants. Through planting trees or plants at school, they can meet new friends, gain status and expand their knowledge. ",
        },
      ],
    };
  },
};
</script>

<style lang="scss" module>
.wrapper {
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  background-image: url("../assets/images/bg2.png");
  @include custom(930) {
    background-image: none;
  }
  padding: 5.625rem 0;
  background-color: $light-brown;
  margin-top: 5rem;
  .container {
    @include container;
    .title {
      @include F64-900;
      text-align: center;
      margin: 0 0 2rem 0;
      @include custom(1080) {
        font-size: 3rem;
      }
      @include custom(750) {
        font-size: 2.5rem;
        line-height: 100%;
      }
      @include custom(500) {
        font-size: 2rem;
        margin: 0 0 1rem 0;
        line-height: 100%;
      }
    }
    .content {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 1.5rem;
      margin: 0 0 10rem 0;
      @include custom(1010) {
        margin: 0 0 8rem 0;
      }
      @include custom(670) {
        margin: 0 0 5rem 0;
      }
      @include custom(970) {
        grid-template-columns: 1fr 1fr;
        .column:last-child {
          grid-column: 1/ -1;
        }
      }
      @include custom(660) {
        display: block;
        .column {
          margin: 0 0 2rem 0;
        }
        .column:last-child {
          margin: 0;
        }
      }
      .subtitle {
        @include F36-600;
        @include custom(1060) {
          font-size: 1.8rem;
        }
      }
      .text {
        @include F28-400;
        @include custom(1060) {
          font-size: 1.5rem;
        }
      }
    }
    .video {
      margin-bottom: -15rem;
      max-width: 88.25rem;
      height: 42.375rem;
      @include custom(1010) {
        height: 30rem;
        margin-bottom: -10rem;
      }
      @include custom(670) {
        height: 20rem;
        margin-bottom: 0;
      }
      & iframe {
        object-fit: cover;
        width: 100%;
        height: 100%;
        border-radius: 1.25rem;
      }
    }
  }
}
</style>
