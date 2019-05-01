<template>
  <div
    :style="style"
    class="item"
  />
</template>

<script>
export default {
  name: 'Item',
  props: {
    item: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      photo: this.item.links[0].href,
      title: this.item.data[0].title,
    };
  },
  computed: {
    style() {
      return {
        backgroundImage: `url("${this.photo}")`,
      };
    },
  },
};
</script>

<style lang="scss" scoped>
  .item {
    background-position: 50%;
    background-size: cover;
    background-repeat: no-repeat;
    width: 40vw;
    height: 250px;

    @media (min-width: 768px) {
      width: 25vw;
    }
  }
</style>
