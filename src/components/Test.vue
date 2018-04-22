<template>
  <div class="el-container">
    <top-nav></top-nav>
  </div>
</template>

<script>
import TopNav from './TopNav';

export default {
  name: 'test',
  components: { TopNav },
  methods: {
    startHacking() {
      this.$notify({
        title: 'It works!',
        type: 'success',
        message: 'We\'ve laid the ground work for you. It\'s time for you to build something epic!',
        duration: 5000,
      });
    },
  },
};
</script>

<style lang="scss" scoped>
  @import "../common.scss";
</style>
