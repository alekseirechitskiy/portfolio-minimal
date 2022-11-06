<template>
  <swiper
    class="swiper"
    :breakpoints="{
    320: {
      slidesPerView: 1,
    },
    768: {
      slidesPerView: 2,

      spaceBetween: 10

    },
    1024: {
      slidesPerView: 2,
    },
    1280: {
      slidesPerView: 3,
    }
  }"
    :modules="modules"
    :space-between="12"
    navigation
  >
    <swiper-slide>
      <a class="swiper__item-link" href="#">
        <div class="swiper__item-link-hover">
          <span class="swiper__item-link-text">view project</span>
        </div>
        <img class="swiper__item-image" src="../assets/about-1.jpg" alt="slide #1">
      </a>
    </swiper-slide>
    <swiper-slide>
      <a class="swiper__item-link" href="#">
        <div class="swiper__item-link-hover">
          <span class="swiper__item-link-text">view project</span>
        </div>
        <img class="swiper__item-image" src="../assets/about-2.jpg" alt="slide #2">
      </a>
    </swiper-slide>
    <swiper-slide>
      <a class="swiper__item-link" href="#">
        <div class="swiper__item-link-hover">
          <span class="swiper__item-link-text">view project</span>
        </div>
        <img class="swiper__item-image" src="../assets/about-3.jpg" alt="slide #3">
      </a>
    </swiper-slide>
    <swiper-slide>
      <a class="swiper__item-link" href="#">
        <div class="swiper__item-link-hover">
          <span class="swiper__item-link-text">view project</span>
        </div>
        <img class="swiper__item-image" src="../assets/about-2.jpg" alt="slide #4">
      </a>
    </swiper-slide>
    <swiper-slide>
      <a class="swiper__item-link" href="#">
        <div class="swiper__item-link-hover">
          <span class="swiper__item-link-text">view project</span>
        </div>
        <img class="swiper__item-image" src="../assets/about-3.jpg" alt="slide #5">
      </a>
    </swiper-slide>
  </swiper>
</template>
<script>
  import { Navigation} from 'swiper';
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';
  // Import Swiper styles
  import 'swiper/css';
  import 'swiper/css/navigation';

  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Navigation],
      };
    },
  };
</script>
<style lang="scss">

.swiper {
  padding-top: 40px;
}

.swiper__item-image {
  width: 100%;
  object-fit: cover;
  height: 358px;
}

.swiper-button-prev {
  top: 20px;
  // left: 60%;
  left: auto;
  right: 40px;
  height: 32px;
  width: 32px;

    @media #{$screen-1024} {
      left: 60%;
    }

  &::after {
    font-size: 0;
    background-image: url("../assets/icons/arrow-left.svg");
    height: 32px;
    width: 32px;
  }
}

.swiper-button-next {
  height: 32px;
  width: 32px;
  top: 20px;
  right: 0;

    @media #{$screen-1024} {
      left: 64%;
    }


  &::after {
    font-size: 0;
    background-image: url("../assets/icons/arrow-right.svg");
    height: 32px;
    width: 32px;
  }
}

  .swiper__item-link {
    display: block;
    height: 358px;
    position: relative;
  }

  .swiper__item-link-hover {
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    position: absolute;
    content: "";
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    background-color: rgba(0,0,0, 0.5);
    transition: opacity 0.3s;
  }
  
  .swiper__item-link:hover {
    .swiper__item-link-hover {
      opacity: 1;
    }
  }

  .swiper__item-link-text {
    font-family: 'Space Grotesk';
    font-weight: 500;
    font-size: 20px;
    line-height: 28px;
    letter-spacing: -0.25px;
    color: #FFFFFF;
    padding-left: 32px;
    position: relative;

    @media #{$screen-1024} {
      font-size: 24px;
      line-height: 31px;
    }


    &::before {
      position: absolute;
      content: "";
      width: 24px;
      height: 24px;
      top: 4px;
      left: 0;
      background-image: url('../assets/icons/view-project.svg');
    }
  }

.dark-mode {
  .swiper-button-prev::after {
    background-image: url("../assets/icons/arrow-left-white.svg");
  }
  
  .swiper-button-next::after {
    background-image: url("../assets/icons/arrow-right-white.svg");
  }
}




</style>