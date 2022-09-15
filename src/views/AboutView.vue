<template>
  <div class="about">
    <h1 class="about__title title">Simply said,<br>I love design and code.</h1>
    <h2 class="about__subtitle subtitle">And... I love food</h2>
    <p class="about__text text">Based in Moskow, Russia, sometimes in Minsk, Belarus.<br>
    I am currently exploring the <strong>UI/UX design, Tailwind-css</strong> and <strong>Vue 3</strong>.</p>
    <p class="about__text text">I am either smiling or looking super serious. If it's the latter one, I am probably thinking about food.</p>
    <div class="about__slider slider">
      <div class="slider__buttons">
        <button class="slider__button slider__button--disabled slider__button-prev"></button>
        <button class="slider__button slider__button-next"></button>
      </div>
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
    </div>
  </div>
</template>

<style lang="scss">
  .about {
    display: flex;
    flex-direction: column;
    width: 100%;
    padding: 24px;
    text-align: left;
    // padding-top: 138px;
    padding-top: 9%;
}

  .about__title {
    margin: 0;
    margin-bottom: 16px;
    font-weight: 900;
    font-size: 48px;
    line-height: 117%;
    letter-spacing: -0.8px;
    color: #000201;
  }

  .about__subtitle {
    font-family: 'Space Grotesk', Helvetica, Arial, sans-serif;
    font-weight: 700;
    font-size: 24px;
    line-height: 31px;
    color: #D3902A;
    margin: 0;
    margin-bottom: 40px;
  }

  .about__text {
    font-family: 'Space Grotesk', Helvetica, Arial, sans-serif;
    font-weight: 400;
    font-size: 24px;
    line-height: 150%;
    letter-spacing: -0.25px;
    max-width: 508px;
    margin: 0;
    margin-bottom: 24px;
    color: rgba(0, 2, 1, 0.6);

    & strong {
      color: rgba(0, 2, 1);
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
    position: fixed;
    bottom: 37%;
    right: 24px;
    display: flex;
    z-index: 1;
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
    display: none;
    position: absolute;
    content: "";
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    background-color: rgba(0,0,0, 0.5);
  }
  
  .slider__item-link:hover {
    .slider__item-link-hover {
      display: flex;
      align-items: center;
      justify-content: center;
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
      background-image: url('../assets/view-project.svg');
    }
  }

  .slider__item-image {
    object-fit: cover;
    object-position: center;
  }
</style>
