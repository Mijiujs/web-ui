<template>
  <div class="login">
    <div class="box">
      <h2  @click="login">登录</h2>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {}
  },
  methods: {
    login () {
      this.$router.push({ path: '/home' })
    }
  }
}
</script>
<style lang="scss" scoped>
.login {
  background: linear-gradient(to right, #74ebd5, #acb6e5);
  width: 100vw;
  height: 100vh;
  .box {
    position: absolute;
    top: 50%;
    left: 50%;
    margin-top: -300px;
    margin-left: -200px;
    width: 400px;
    height: 600px;
    background-size: 100% 100%;
    border: 10px solid #fff;
    box-shadow: 0 0 20px rgb(167, 187, 179);
    text-align: center;
    color: #fff;
    background: url("../assets/back.jpg") no-repeat;
    h2 {
      margin-top: 140px;
    }
    .el-form {
      margin: 20px 80px;
      .el-button {
        padding: 10px 104px;
        color: #74ebd5;
      }
      .operate {
        margin-top: 10px;
        display: flex;
        font-size: 14px;
        .item {
          flex: 1;
          text-decoration: underline;
          &:hover {
            color: #74ebd5;
          }
        }
      }
    }
  }
}
</style>
