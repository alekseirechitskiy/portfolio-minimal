<template>
  <div class="about">
    <!-- <h1 class="about__title title">Simply said,<br>I love design and code.</h1>
    <h2 class="about__subtitle subtitle">And... I love music</h2>
    <Text />
    <p class="about__text text">Based in Moskow, Russia, sometimes in Minsk, Belarus.<br>
    I am currently exploring the <strong>UI/UX design, Tailwind-css</strong> and <strong>Vue 3</strong>.</p>
    <p class="about__text text">
      I am either smiling or looking super serious. If it's the latter one, I am probably thinking about food.
    </p> -->
    <div class="about__slider-wrapper">
      <!-- <div class="slider__buttons">
        <button class="slider__button slider__button--disabled slider__button-prev swiper-button-prev"></button>
        <button class="slider__button slider__button-next swiper-button-next"></button>
      </div> -->
      <Swiper/>
      <!-- <div class="about__slider slider">
        <div class="slider__item">
          <a class="slider__item-link" href="#">
            <div class="slider__item-link-hover">
              <span class="slider__item-link-text">view project</span>
            </div>
            <img class="slider__item-image" src="../assets/about-1.jpg" alt="slide #1" width="486" height="358">
          </a>
        </div>
        <div class="slider__item">
          <a class="slider__item-link" href="#">
            <div class="slider__item-link-hover">
              <span class="slider__item-link-text">view project</span>
            </div>
            <img class="slider__item-image" src="../assets/about-2.jpg" alt="slide #2" width="486" height="358">
          </a>
        </div>
        <div class="slider__item">
          <a class="slider__item-link" href="#">
            <div class="slider__item-link-hover">
              <span class="slider__item-link-text">view project</span>
            </div>
            <img class="slider__item-image" src="../assets/about-3.jpg" alt="slide #3" width="486" height="358">
          </a>
        </div>
      </div> -->
    </div>
  </div>
</template>

<script>
import Text from '../components/Text';
import Swiper from '../components/Swiper';
export default {
  name: 'About',
  components: {
    Text,
    Swiper
  }
}
</script>

<style lang="scss">
  .about {
    box-sizing:border-box;
    width: 100vw;
    padding: 15px;
    text-align: left;
    background-color: var(--bg-color);

    @media #{$desktop}{
      width: 100%;
      padding: 24px;
      padding-top: 130px;
      height: auto;
      margin-left: 22%;
    }
  }


  .about__title {
    margin: 0;
    margin-bottom: 16px;
    max-width: 300px;
    @media #{$desktop}{
      max-width: 100% ;
    }
  }

  .about__subtitle {
    font-family: 'Space Grotesk', Helvetica, Arial, sans-serif;
    font-weight: 700;
    font-size: 22px;
    line-height: 31px;
    color: #D3902A;
    margin: 0;
    margin-bottom: 20px;

    @media #{$desktop}{
      font-size: 24px;
      margin-bottom: 40px;
    }
  }

  .about__text {
    font-family: 'Space Grotesk', Helvetica, Arial, sans-serif;
    font-weight: 400;
    letter-spacing: -0.25px;
    max-width: 508px;
    margin: 0;
    margin-bottom: 24px;
    color: var(--text-color);

    & strong {
      color: var(--title-color);
    }
  }

  .about__slider-wrapper {
    position: relative;
    margin-top: 40px;
    @media #{$desktop}{
      margin-top: 60px;
    }

  }

  .about__slider {
    margin-top: auto;
  }

  .slider {
    display: flex;
    width: 100%;
    overflow: hidden;
    position: relative;
  }
  
  .slider__buttons {
    position: absolute;
    top: -35px;
    right: 0;
    display: flex;
    z-index: 1;

    @media #{$desktop}{
      left: 65%;
      right: 0;
    }
  }

  .slider__button {
    width: 32px;
    height: 32px;
    border: none;
    background-color: transparent;
    background-repeat: no-repeat;
    background-position: center;
    cursor: pointer;
  }

  .slider__button-prev {
    background-image: url("../assets/icons/arrow-left.svg");
  }

  .slider__button-next {
    background-image: url("../assets/icons/arrow-right.svg");
  }

  .slider__button-prev.slider__button--disabled {
    background-image: url("../assets/icons/arrow-left-disabled.svg");
  }

  .slider__button-next.slider__button--disabled {
    background-image: url("../assets/icons/arrow-right-disabled.svg");
  }

  .slider__item {
    margin-right: 12px;
  }

  .slider__item-link {
    display: block;
    height: 358px;
    position: relative;
  }

  .slider__item-link-hover {
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
  
  .slider__item-link:hover {
    .slider__item-link-hover {

      opacity: 1;

    }
  }

  .slider__item-link-text {
    font-family: 'Space Grotesk';
    font-weight: 500;
    font-size: 24px;
    line-height: 31px;
    letter-spacing: -0.25px;
    color: #FFFFFF;
    padding-left: 32px;
    position: relative;

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

  .slider__item-image {
    object-fit: cover;
    object-position: center;
  }
</style>
