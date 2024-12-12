<template>
  <div :class="$style.container">
    <div :class="$style.title">Learning Resources & Activities</div>
    <div :class="$style.subtitle">
      At Resiliency Gardens, we're always on the lookout for helpful print and
      video resources for children and adults to make gardening fun and
      educational. Take a look at these topics and click to learn more and
      download a free printable
    </div>
    <div :class="$style.content">
      <div :class="$style.card" v-for="item in cards" :key="item.title">
        <div :class="$style.image">
          <img :src="item.image" alt="" />
        </div>
        <div :class="$style.info">
          <div :class="$style.text">{{ item.text }}</div>
          <div :class="$style.actions">
            <div :class="$style.file">
              Download
              <img src="/icons/download.svg" alt="" />
            </div>
            <div :class="$style.file">
              Sourcelink
              <img src="/icons/link.svg" alt="" />
            </div>
          </div>
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
          image: "/images/activities/1.png",
          text: "Design and Placing the garden",
          file: "",
          link: "",
        },
        {
          image: "/images/activities/2.png",
          text: "Starting a School Garden Program",
          file: "",
          link: "",
        },
        {
          image: "/images/activities/3.png",
          text: "Vermi-composting for Plant & Planet health",
          file: "",
          link: "",
        },
        {
          image: "/images/activities/4.png",
          text: "Sustainable Gardening Ideasfrom Around the Globe",
          file: "",
          link: "",
        },
      ],
    };
  },
};
</script>

<style lang="scss" module>
.container {
  @include container;
  padding-top: 13rem;
  @include custom(670) {
    padding-top: 4rem;
  }
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
  .subtitle {
    @include F36-500;
    line-height: 2.625rem;
    text-align: center;
    margin-bottom: 3rem;
    @include custom(970) {
      font-size: 1.8rem;
    }
    @include custom(620) {
      font-size: 1.5rem;
      text-align: left;
    }
  }
  .content {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 1.5rem;
    @include custom(830) {
      grid-template-columns: 1fr 1fr;
    }
    @include custom(540) {
      grid-template-columns: 1fr;
    }
    .card {
      border: 0.1875rem solid $black;
      border-radius: 1.25rem;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      .image {
        max-width: 30rem;
        height: 29.375rem;
        margin: 0 0 6.25rem 0;
        & img {
          width: 100%;
          height: 100%;
          border-radius: 1.25rem 1.25rem 0 0;
        }
        @include custom(1140) {
          height: 23rem;
          margin: 0 0 4rem 0;
        }
        @include custom(960) {
          height: 18rem;
        }
        @include custom(830) {
          margin: 0 0 2rem 0;
          height: 22rem;
        }
        @include custom(620) {
          margin: 0 0 2rem 0;
          height: 18rem;
        }
        @include custom(540) {
          max-width: 20rem;
          height: 100%;
          margin: 0 auto;
          padding: 1rem;
          & img {
            border-radius: 1.25rem;
          }
        }
      }
      .info {
        padding: 1rem;
        .text {
          text-align: left;
          @include F28-500;
          margin-bottom: 1rem;
          @include custom(960) {
            font-size: 1.5rem;
          }
          @include custom(620) {
            font-size: 1.2rem;
          }
        }

        .actions {
          display: flex;
          align-items: center;
          justify-content: space-between;
          padding-top: 1rem;
          border-top: 3px solid $black;
          @include custom(1080) {
            flex-direction: column;
            gap: 1rem;
            align-items: flex-start;
          }
          .file {
            @include F28-500;
            font-size: 1.625rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            cursor: pointer;
          }
        }
      }
    }
    .video {
      grid-column: 2/-1;
      @include custom(830) {
        grid-column: 1/-1;
      }
      & iframe {
        width: 100%;
        height: 100%;
        border-radius: 1.25rem;
        @include custom(830) {
          height: 18rem;
          max-width: 100%;
        }
      }
    }
  }
}
</style>
