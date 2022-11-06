<template>
  <div class="works">
    <h1 class="works__title title">Works</h1>
    <p class="works__text text">Repository of projects that I worked before.</p>
    <div class="works__tabs tabs">
      <ul class="tabs__list">
        <li @click="selectTab" class="tabs__item tabs__item--active">
          <a  class="tabs__link" href="#">All</a>
        </li>
        <li class="tabs__item">
          <a class="tabs__link" href="#">Markups</a>
        </li>
        <li class="tabs__item">
          <a class="tabs__link" href="#">Vanila JS</a>
        </li>
        <li class="tabs__item">
          <a class="tabs__link" href="#">Vue</a>
        </li>
        <li class="tabs__item">
          <a class="tabs__link" href="#">React</a>
        </li>
      </ul>
      <ul class="works__list">
        <li class="works__item">
          <a class="works__item-link" href="#">
            <div class="works__item-link-hover">
              <span class="works__item-link-text">view project</span>
            </div>
          <img class="works__item-image" src="../assets/about-3.jpg" alt="slide #2" width="328" height="246">
          </a>
        </li>
        <li class="works__item">
          <a class="works__item-link" href="#">
            <div class="works__item-link-hover">
              <span class="works__item-link-text">view project</span>
            </div>
          <img class="works__item-image" src="../assets/works-2.jpg" alt="slide #2" width="328" height="246">
          </a>
        </li>
        <li class="works__item">
          <a class="works__item-link" href="#">
            <div class="works__item-link-hover">
              <span class="works__item-link-text">view project</span>
            </div>
          <img class="works__item-image" src="../assets/works-3.jpg" alt="slide #2" width="328" height="246">
          </a>
        </li>
        <li class="works__item">
          <a class="works__item-link" href="#">
            <div class="works__item-link-hover">
              <span class="works__item-link-text">view project</span>
            </div>
          <img class="works__item-image" src="../assets/works-4.jpg" alt="slide #2" width="328" height="246">
          </a>
        </li>
        <li class="works__item">
          <a class="works__item-link" href="#">
            <div class="works__item-link-hover">
              <span class="works__item-link-text">view project</span>
            </div>
          <img class="works__item-image" src="../assets/works-5.jpg" alt="slide #2" width="328" height="246">
          </a>
        </li>
        <li class="works__item">
          <a class="works__item-link" href="#">
            <div class="works__item-link-hover">
              <span class="works__item-link-text">view project</span>
            </div>
          <img class="works__item-image" src="../assets/works-6.jpg" alt="slide #2" width="328" height="246">
          </a>
        </li>
        <li class="works__item">
          <a class="works__item-link" href="#">
            <div class="works__item-link-hover">
              <span class="works__item-link-text">view project</span>
            </div>
          <img class="works__item-image" src="../assets/works-5.jpg" alt="slide #2" width="328" height="246">
          </a>
        </li>
        <li class="works__item">
          <a class="works__item-link" href="#">
            <div class="works__item-link-hover">
              <span class="works__item-link-text">view project</span>
            </div>
          <img class="works__item-image" src="../assets/works-3.jpg" alt="slide #2" width="328" height="246">
          </a>
        </li>
        <li class="works__item">
          <a class="works__item-link" href="#">
            <div class="works__item-link-hover">
              <span class="works__item-link-text">view project</span>
            </div>
          <img class="works__item-image" src="../assets/about-3.jpg" alt="slide #2" width="328" height="246">
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>


<script>
export default {
  name: 'Works',
  components: {
  },
  methods: {
    selectTab(){
      this.classList.remove('tabs__item--active');
    }
  },
}
</script>

<style lang="scss">
  .works {
    box-sizing: border-box;
    width: 100%;
    padding: 15px;
    text-align: left;

      @media #{$screen-1024}{
      padding: 24px;
      padding-top: 130px;
      height: auto;
      // margin-left: 384px;
    }
  }

  .works__title {
    margin: 0;
    margin-bottom: 16px;
    font-weight: 900;
    font-size: 48px;
    line-height: 117%;
    letter-spacing: -0.8px;
    color: var(--title-color);
  }

  .works__text {
    font-family: 'Space Grotesk', Helvetica, Arial, sans-serif;
    font-weight: 400;
    font-size: 24px;
    line-height: 150%;
    letter-spacing: -0.25px;
    max-width: 508px;
    margin: 0;
    margin-bottom: 54px;
    color: var(--text-color);

    & strong {
      color: var(--title-color);
    }
  }

  .works__tabs{
    padding-bottom: 24px;
    width: 100%;
  }

  .works__list {
    // box-sizing: border-box;

    width: 100%;
    margin: 0;
    margin-top: 40px;
    padding: 0;
    list-style: none;
    display: grid;
    grid-template-columns: repeat(1, 1fr);
    // grid-template-rows: repeat(3, 1fr);
    grid-gap: 15px;
    overflow-y: visible;

    @media #{$screen-500} {
      grid-template-columns: repeat(2, 1fr);
    }

    @media #{$screen-1024} {
      grid-template-columns: repeat(2, 1fr);
      grid-gap: 24px;
    }

    @media #{$screen-1280} {
      grid-template-columns: repeat(3, 1fr);
      grid-gap: 24px;
    }
  }

  .works__item {
    box-sizing: border-box;

    width: 100%;
  }

  .works__item-link {
    display: block;
    // height: 246px;
    // height: 246px;
    position: relative;
  }

  .works__item-link-hover {
    // display: none;
    opacity: 0;
    transition: opacity 0.3s;
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    content: "";
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    background-color: rgba(0,0,0, 0.5);
  }
  
  .works__item-link:hover {
    .works__item-link-hover {
      opacity: 1;
      display: flex;
      align-items: center;
      justify-content: center;
    }
  }

  .works__item-link-text {
    font-family: 'Space Grotesk';
    font-weight: 500;
    font-size: 18px;
    line-height: 24px;
    letter-spacing: -0.25px;
    color: #FFFFFF;
    padding-left: 32px;
    position: relative;

     @media #{$screen-1024} {
    font-size: 20px;
    line-height: 26px;
    }

    &::before {
      position: absolute;
      content: "";
      width: 24px;
      height: 24px;
      top: 3px;
      left: 0;
      background-image: url('../assets/icons/view-project.svg');
    }
  }

  .works__item-image {
    width: 100%;
    height: auto;
    vertical-align: bottom;
    object-fit: cover;
    object-position: center;
  }

  .tabs {
    display: inline-block;
  }

  .tabs__list {
    margin: 0;
    padding: 0;
    padding-bottom: 15px;
    list-style: none;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    justify-content: flex-start;
    border-bottom: 1px solid var(--tabs-border);

    @media #{$screen-500} {
      flex-direction: row;
    }
  }

  .tabs__item {
    padding: 5px 0;

    border-bottom: 1px solid transparent;
      @media #{$screen-500} {
    padding: 0 20px;

      }


    &:first-child{
      padding-left: 0;
    }

    &:last-child{
      padding-right: 0;
    }
  }

  .tabs__item--active {
    position: relative;

    &::after {
      display: none;

      @media #{$screen-500} {
        position: absolute;
        content: "";
        width: 100%;
        height: 1px;
        top: 36px;
        left: 0;
        background-color: var(--title-color);
      }
    }
  }

  .tabs__item--active .tabs__link {
    color: var(--title-color);
  }

  .tabs__link {
    white-space: nowrap;
    text-decoration: none;
    font-family: 'Space Grotesk';
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 20px;
    letter-spacing: -0.25px;
    color: var(--text-color);
  }

</style>
