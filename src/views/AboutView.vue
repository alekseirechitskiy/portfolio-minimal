<template>
  <div class="about">
    <h1 class="about__title title">Simply said,<br>I love design and code.</h1>
    <h2 class="about__subtitle subtitle">And... I love music</h2>
    <p class="about__text text"> Based in the beautiful city of Bali, Indonesia.<br>
    I am currently exploring the <strong>UI/UX design, Tailwind-css</strong> and <strong>Vue 3</strong>.</p>
    <p class="about__text text">
      I am either smiling or looking super serious. If it's the latter one, I am probably thinking about food.
    </p>
    <Swiper/>
  </div>
</template>

<script>
import Swiper from '../components/Swiper';
export default {
  name: 'About',
  components: {
    Swiper
  }
}
</script>

<style lang="scss" scoped>
.about {
  box-sizing:border-box;
  width: 100vw;
  padding: 15px;
  padding-bottom: 50px;
  text-align: left;
  background-color: var(--bg-color);

  @media #{$screen-1024} {
    width: 100%;
    padding: 130px 24px 24px 24px;
    height: auto;
  }
}

.about__title {
  margin: 0;
  margin-bottom: 16px;
  max-width: 300px;

  @media #{$screen-1024} {
    max-width: 100% ;
  }
}

.about__subtitle {
  font-family: 'Space Grotesk', Helvetica, Arial, sans-serif;
  font-weight: 700;
  font-size: 22px;
  line-height: 31px;
  color: var(--text-color-accent);
  margin: 0;
  margin-bottom: 20px;

  @media #{$screen-1024} {
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
    color: var(--strong-color);
  }
}

</style>
