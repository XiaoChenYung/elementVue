<template>
  <div class="top-nav">
    <el-row class="content">
      <el-col :span="12">
        <div class="logo-content">
          <img class="logo" src="../assets/logo.png"/>
        </div>
        <el-dropdown @command="handleCommand" class="drop-down">
          <span class="el-dropdown-link">{{ $t("el.colorpicker.confirm") }}
            <i class="el-icon-arrow-down el-icon--right"></i>
          </span>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item command="en">English</el-dropdown-item>
            <el-dropdown-item command="zh">简体中文</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </el-col>
      <el-col :span="12">

      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'TopNav',
  data() {
    return {
      activeIndex: '1',
      activeIndex2: '1',
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    },
    handleCommand(command) {
      command === 'zh' ? this.$i18n.locale = 'zh' : this.$i18n.locale = 'en';
      // this.$message('click on item ' + command);
    },
  },
};
</script>

<style lang="scss" scoped>
  .top-nav {
    height: 80px;
    width: 1920px;
    margin: 0 auto;
    background: darkgray;
  }
  .logo-content {
    float: left;
  }
  .logo {
    width: 60px;
    height: 30px;
  }
  .drop-down {
    margin-left: 30px;
    float: left;
  }
</style>
