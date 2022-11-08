<template>
  <div class="wrapper">
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
      <swiper-slide 
        class="swiper__slide"
        v-for="slide in dataBase.slice(0, 5)" :key="slide.id">
        <CaseCard 
          :caseImage="slide.imagePath"
          :caseImageDescription="slide.imageDescription"
        />
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
  // Import Swiper
  import { Navigation} from 'swiper';
  import { Swiper, SwiperSlide } from 'swiper/vue';
  import 'swiper/css';
  import 'swiper/css/navigation';
  // Import my components
  import CaseCard from './CaseCard.vue';
  import data from "./data.js";

  export default {
    data(){
      return{
        dataBase: data,
      }
    },
    components: {
      Swiper,
      SwiperSlide,
      CaseCard
    },
    setup() {
      return {
        modules: [Navigation],
      };
    },
  };
</script>
<style lang="scss" >
.wrapper {
  position: relative;

  @media #{$screen-1024} {
    padding-right: 52px;
  }
}

.swiper {
  padding-top: 40px;
}

.swiper__slide {
  width: 100%;
}

.swiper-button-prev {
  top: 20px;
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

.dark-mode {
  .swiper-button-prev::after {
    background-image: url("../assets/icons/arrow-left-white.svg");
  }

  .swiper-button-next::after {
    background-image: url("../assets/icons/arrow-right-white.svg");
  }
}

</style>