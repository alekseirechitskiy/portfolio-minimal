<template>
  <div class="works">
    <h1 class="works__title title">Works</h1>
    <p class="works__text text">Repository of projects that I worked before.</p>
    <div class="works__tabs tabs">
      <ul class="tabs__list">
        <li class="tabs__item tabs__item--active">
          <a class="tabs__link" href="#">All</a>
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
    </div>
  </div>
</template>

<style lang="scss">
  .works {
    width: 100%;
    padding: 24px;
    text-align: left;
    padding-top: 138px;
  }

  .works__title {
    margin: 0;
    margin-bottom: 16px;
    font-weight: 900;
    font-size: 48px;
    line-height: 117%;
    letter-spacing: -0.8px;
    color: #000201;
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
    color: rgba(0, 2, 1, 0.6);

    & strong {
      color: rgba(0, 2, 1);
    }
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
    justify-content: flex-start;
    border-bottom: 1px solid rgba(0, 0, 0, 0.15);
  }

  .tabs__item {
    padding: 0 20px;
    border-bottom: 1px solid transparent;

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
      position: absolute;
      content: "";
      width: 100%;
      height: 1px;
      top: 36px;
      left: 0;
      background-color: rgba(0, 2, 1);
    }
  }

  .tabs__item--active .tabs__link {
    color:rgba(0, 2, 1);
  }

  .tabs__link {
    text-decoration: none;
    font-family: 'Space Grotesk';
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 20px;
    letter-spacing: -0.25px;
    color: rgba(0, 2, 1, 0.6);
  }

</style>
