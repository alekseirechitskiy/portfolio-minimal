<template>
  <ul class="tabs__list">
    <li class="tabs__item" @click="setActive('tab-1')" :class="{'tabs__item--active' : isActive('tab-1')}">
      <div class="tabs__link" >All</div>
    </li>
    <li class="tabs__item" @click="setActive('tab-2')" :class="{'tabs__item--active' : isActive('tab-2')}">
      <div class="tabs__link">Markups</div>
    </li>
    <li class="tabs__item" @click="setActive('tab-3')" :class="{'tabs__item--active' : isActive('tab-3')}">
      <div class="tabs__link">Vanila JS</div>
    </li>
    <li class="tabs__item" @click="setActive('tab-4')" :class="{'tabs__item--active' : isActive('tab-4')}">
      <div class="tabs__link">Vue</div>
    </li>
    <li class="tabs__item" @click="setActive('tab-5')" :class="{'tabs__item--active' : isActive('tab-5')}">
      <div class="tabs__link">React</div>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      activeTab: 'tab-1'
    }
  },
  methods: {
    setActive(tab){
      this.activeTab = tab;
    },
    isActive(tab) {
      return this.activeTab === tab;
    }
  }
}
</script>

<style lang="scss" scoped>
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
  position: relative;

  &::after {
    display: none;

    @media #{$screen-500} {
      display: block;
      position: absolute;
      content: "";
      width: 100%;
      height: 1px;
      top: 35px;
      left: 0;
      opacity: 0;
      transition: all 0.3s;
    }
  }

  @media #{$screen-500} {
    padding: 0 20px;
  }

  &:first-child{
    padding-left: 0;
  }
}

.tabs__item.tabs__item--active {
  position: relative;

  &::after {
    display: none;

    @media #{$screen-500} {
      display: block;
      position: absolute;
      content: "";
      width: 100%;
      height: 1px;
      top: 35px;
      left: 0;
      background-color: var(--title-color);
      opacity: 1;
      transition: all 0.3s;
    }
  }
}

.tabs__item--active .tabs__link {
  font-weight: 900;
  color: var(--title-color);
  transition: all 0.3s;

  @media #{$screen-500} {
    font-weight: 400;
  }
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
  cursor: pointer;
}

</style>