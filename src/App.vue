<template>
  <div id="app">

  <el-button @click="drawer = true" type="primary" style="margin-left: 16px;">
    AI採寸
  </el-button>

  <el-drawer
    title="AI採寸"
    :visible.sync="drawer"
    :direction="rtl"
    :before-close="handleClose">
    <iframe src="https://aobabd.wordpress.com/" frameborder="0" width="100%" height="600px"></iframe>
  </el-drawer>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        drawer: false,
        direction: 'rtl',
      };
    },
    methods: {
      handleClose(done) {
        this.$confirm('确认关闭？')
        // eslint-disable-next-line
          .then(_ => {
            done();
          })
          // eslint-disable-next-line
          .catch(_ => {});
      }
    }
  };
</script>


