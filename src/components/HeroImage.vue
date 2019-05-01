<template>
  <div class="heroImage" />
</template>

<script>
export default {
  name: 'HeroImage',
};
</script>

<style lang="scss" scoped>
  .heroImage {
    top: 0;
    z-index: -1;
    height: 100vh;
    width: 100%;
    position: fixed;
    background-image: url('../assets/heroimage.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 80% 0;
  }

  .heroImage::after {
    content: '';
    background: rgba($color: #000000, $alpha: .2);
    position: absolute;
    top: 0;
    left: 0;
    z-index: 1;
    width: 100%;
    height: 100vh;
  }
</style>
