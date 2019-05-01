<template>
  <div class="searchWrapper">
    <input
      id="search"
      name="search"
      :value="value"
      :class="{ dark }"
      @input="handleChange"
    >
  </div>
</template>

<script>
export default {
  name: 'SearchInput',
  props: {
    value: {
      type: String,
      required: true,
    },
    dark: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    handleChange(e) {
      this.$emit('input', e.target.value);
    },
  },
};
</script>

<style lang="scss" scoped>
      input {
       margin-top: 50px;
       display: flex;
       width: 250px;
       height: 30px;
       border: 0;
       background: none;
       border-bottom: 1px solid white;
       transition: box-shadow .3s ease-out;
       text-align: center;
       font-size: 18px;
       font-weight: 300;
       color: white;
     }

     input:focus {
       outline: none;
       box-shadow: 0 10px 10px -8px rgba(255, 255, 255, .2);
     }

     input:active {
       outline: none;
     }

     .dark {
       color: #1e3d4a;
       border-bottom-color: #1e3d4a;
     }

     .dark:focus {
       outline: none;
       box-shadow: 0 10px 10px -8px rgba(#1e3d4a, .2);
     }
</style>
