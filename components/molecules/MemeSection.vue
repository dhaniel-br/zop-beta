<template>
  <div class="meme-section">
    <div class="swiper-container">
      <div class="swiper-wrapper">
        <!-- Slides -->
        <div class="swiper-slide">
          <img src="@/assets/img/memes/meme1.jpg" alt="meme" class="media" />
        </div>
        <div class="swiper-slide">
          <img src="@/assets/img/memes/meme2.jpeg" alt="meme" class="media" />
        </div>
        <div class="swiper-slide">
          <img src="@/assets/img/memes/meme3.jpg" alt="meme" class="media" />
        </div>
        <div class="swiper-slide">
          <video src="@/assets/img/memes/meme6.mp4" controls class="media" />
        </div>
      </div>
      <div class="swiper-button-prev"></div>
      <div class="swiper-button-next"></div>
    </div>
  </div>
</template>

<script>
// eslint-disable-next-line import/no-named-as-default
import Swiper, { Navigation, Pagination } from 'swiper'
import 'swiper/swiper-bundle.css'

Swiper.use([Navigation, Pagination])

export default {
  mounted() {
    // eslint-disable-next-line no-new
    new Swiper('.swiper-container', {
      loop: true,
      pagination: {
        el: '.swiper-pagination'
      },
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev'
      },
      scrollbar: {
        el: '.swiper-scrollbar'
      }
    })
  },
  methods: {
    onSwiper(swiper) {
      console.log(swiper)
    },
    onSlideChange() {
      console.log('slide change')
    }
  }
}
</script>

<style lang="scss" scoped>
.meme-section {
  display: flex;
  align-items: center;
  gap: 1rem;
  .swiper-container {
    width: 960px;
    height: 612px;
    @include screen('medium') {
      width: 375px;
      height: 210px;
    }
    .media {
      width: 100%;
      height: 100%;
    }
  }
}
</style>
