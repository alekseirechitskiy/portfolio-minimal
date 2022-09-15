<template>
  <p class="text">sdfsdfgsdfg</p>
</template>

<script>
export default {
  name: 'Text',
  props: {
    text: String
  }

}
</script>

<style scoped lang="scss">
p {
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
</style>