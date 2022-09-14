<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Menu from '@/components/Menu.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    Menu
  }
}
</script>

<style lang="scss">
  .home {
    align-self: stretch;
    // border: 3px solid black;
    width: 100%;
    padding: 24px;
  }
</style>