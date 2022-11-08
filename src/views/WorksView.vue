<template>
  <div class="works">
    <h1 class="works__title title">Works</h1>
    <p class="works__text text">Repository of projects that I worked before.</p>
    <div class="works__tabs tabs">
      <TabsNavigation />
      <ul class="works__list">
        <li lass="works__item" v-for="item in dataBase.slice(3)" :key="item.id">
          <CaseCard 
            :caseImage="item.imagePath"
            :caseImageDescription="item.imageDescription"
        />
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import data from "../components/data.js";
import CaseCard from '../components/CaseCard.vue';
import TabsNavigation from '../components/TabsNavigation.vue';
export default {
  name: 'Works',
  data(){
    return {
      dataBase: data,
    }
  },
  components: {
    CaseCard,
    TabsNavigation
  },
}
</script>

<style lang="scss" scoped>
.works {
  box-sizing: border-box;
  width: 100%;
  padding: 15px;
  text-align: left;

  @media #{$screen-1024} {
    padding: 24px;
    padding-top: 130px;
    height: auto;
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

.works__tabs {
  padding-bottom: 24px;
  width: 100%;
}

.works__list {
  width: 100%;
  margin: 0;
  margin-top: 40px;
  padding: 0;
  list-style: none;
  display: grid;
  grid-template-columns: repeat(1, 1fr);
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
  height: 200px;
}

.works__item-link {
  display: block;
  position: relative;
}

.works__item-link-hover {
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
 
</style>
