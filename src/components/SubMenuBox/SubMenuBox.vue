<template>
  <div class="sub-menu-box">
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    options: {
      type: Object,
      default: function() {
        return {};
      }
    }
  },
  data() {
    return {
      inputValue: this.options.value
    };
  },
  computed: {},
  methods: {}
};
</script>

<style lang="scss" scoped>
@import 'SubMenuBox.scss';
</style>
