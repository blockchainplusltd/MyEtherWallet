<template>
  <div class="sub-menu-box">
    <div class="wrap">
      <div class="menu-title" @click="isOpen = !isOpen">
        {{ options.menuTitle }}
      </div>
      <div v-if="isOpen" class="sub-menu">
        <ul>
          <li v-for="sub in options.subMenus" :key="sub.key">
            <a :href="sub.link">{{ sub.title }}</a>
          </li>
        </ul>
      </div>
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
    }
  },
  data() {
    return {
      isOpen: false
    };
  },
  computed: {},
  watch: {},
  methods: {}
};
</script>

<style lang="scss" scoped>
@import 'SubMenuBox.scss';
</style>
