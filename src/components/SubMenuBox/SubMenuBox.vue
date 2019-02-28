<template>
  <div v-if="isopen" class="sub-menu-box">
    <div class="wrap">
      <slot></slot>
    </div>
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
    },
    isopen: {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
      inputValue: this.options.value
    };
  },
  computed: {},
  watch: {
    isopen(newval) {
      return newval;
    }
  },
  methods: {}
};
</script>

<style lang="scss" scoped>
@import 'SubMenuBox.scss';
</style>
