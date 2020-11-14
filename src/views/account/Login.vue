<template>
  <div class="login">
    <div class="form-wrap">
      <a-form
        label-align="left"
      >
        <a-form-item>
          <label>用户名</label>
          <a-input v-model:value="formConfig.userName" type="text" />
        </a-form-item>
        <a-form-item>
          <label>密码</label>
          <a-input v-model:value="formConfig.userPassword" type="password" />
        </a-form-item>
        <a-form-item>
          <a-button @click="login" type="primary" size="small">
            登录
          </a-button>
        </a-form-item>
      </a-form>
      <div>
        <a class="color-white">忘记密码</a>
        ｜
        <a class="color-white">注册</a>
      </div>
    </div>
  </div>
</template>

<script>
import { reactive } from "vue";
export default {
  name: "Login",
  setup(props) {
    const formConfig = reactive({
      userName: null,
      userPassword: null
    })
    const login = () => {
      console.log(formConfig.userName, formConfig.userPassword);
    }
    return {
      formConfig,
      login
    };
  }
}
</script>

<style lang="scss" scoped>
@import "./style.scss";
</style>
