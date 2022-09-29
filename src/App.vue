<template>
  <div class="application">
    <button 
    class="toggle-menu"
    @click="toggleMenu"
    >
      <span></span>
    </button>
    <div class="menu">
      <nav class="navigation">
        <router-link @click="toggleMenu" class="logo" to="/">alekseirechitskiy.</router-link>
        <router-link @click="toggleMenu" class="navigation__link" to="/">About</router-link>
        <router-link @click="toggleMenu" class="navigation__link" to="/works">Works</router-link>
        <router-link @click="toggleMenu" class="navigation__link" to="/resume">Resume</router-link>
        <router-link @click="toggleMenu" class="navigation__link" to="/contact">Contact</router-link>
        <button 
          class="navigation__button"
          @click="setDarkMode"
        >
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M12 18.5C15.5899 18.5 18.5 15.5899 18.5 12C18.5 8.41015 15.5899 5.5 12 5.5C8.41015 5.5 5.5 8.41015 5.5 12C5.5 15.5899 8.41015 18.5 12 18.5Z" stroke="#000201" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M19.14 19.14L19.01 19.01M19.01 4.99L19.14 4.86L19.01 4.99ZM4.86 19.14L4.99 19.01L4.86 19.14ZM12 2.08V2V2.08ZM12 22V21.92V22ZM2.08 12H2H2.08ZM22 12H21.92H22ZM4.99 4.99L4.86 4.86L4.99 4.99Z" stroke="#000201" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>&nbsp;&nbsp;Switch dark
        </button>
      </nav>
    </div>
    <router-view/>
  </div>

</template>

<script>
export default {
  name: 'App',
  // components:,
  methods: {
    toggleMenu(){
      const menu = document.querySelector('.menu');
      const body = document.querySelector('.body');
        menu.classList.toggle('menu--active');
        body.classList.toggle('overflow-hidden');
    },
    setDarkMode(){
      const body = document.querySelector('.body');
      const about = document.querySelector('.about');
      body.classList.toggle('dark-mode');
      about.classList.toggle('dark-mode');
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Archivo, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  box-sizing: border-box;
  height: 100vh;
  background-color: var(--bg-color);
  position: relative;
  overflow-x: hidden;
}

.application {
  display: flex;
  height: auto;
  max-width: 1440px;
  margin: 0 auto;
  background-color: var(--bg-color);
}

.toggle-menu{
  display: block;
  position: fixed;
  right: 3%;
  top: 15px;
  z-index: 10;
  height: 40px;
  width: 40px;
  padding: 0;
  background: transparent;
  border: none;
  cursor: pointer;

  @media #{$desktop}{
    display: none;
  }

  span{
    display: block;
    background-color: var(--title-color);
    width: 100%;
    height: 5px;
    position: absolute;
    border-radius: 2px;
    box-shadow: 0px 9px var(--title-color), 0px -9px var(--title-color);
  }
}

.menu {
  position: absolute;
  background-color: var(--bg-color);
  height: 100vh;
  z-index: 5;
  width: 384px;
  transform: translateX(-105%);
  transition: transform 0.3s ease-in;

  @media #{$desktop}{
    position: fixed;
    transform: translateX(0%);
    flex-shrink: 0;
    width: 20%;
  }

  &--active {
    transform: translateX(0%);
  }
}

.navigation  {
  box-sizing: border-box;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 24px;
  box-shadow: 0px 0px 10px 3px var(--title-color);

  @media #{$desktop}{
    box-shadow: none;
  }

  .navigation__link {
    text-decoration: none;
    font-weight: 500;
    font-size: 24px;
    line-height: 26px;
    letter-spacing: -0.8px;
    color: var(--link-color);
    margin-bottom: 24px;
    text-transform: lowercase;
    transition: color 0.3s;

    &:hover {
      color: var(--link-color-active);
    }

    &.router-link-exact-active {
      color: var(--link-color-active);
    }
  }
}

.logo {
  margin: 0;
  margin-bottom: 90px;
  font-weight: 700;
  font-size: 24px;
  line-height: 26px;
  letter-spacing: -0.8px;
  color: var(--title-color);
  text-decoration: none;
}

.navigation__button {
  margin-top: auto;
  border: none;
  background-color: transparent;
  display: flex;
  align-items: center;
  cursor: pointer;
  color: var(--title-color);
  svg{
    path{
      stroke: var(--title-color);
    }
  }
}


</style>
