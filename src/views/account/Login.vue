<template>
  <div class="login">
    <div class="form-wrap">
      <a-form
        label-align="left"
      >
        <a-form-item label="用户名">
          <a-input v-model:value="formConfig.userName" type="text" />
        </a-form-item>
        <a-form-item label="密码">
          <a-input v-model:value="formConfig.userPassword" type="password" />
        </a-form-item>
        <a-form-item>
          <a-button @click="login">
            Submit
          </a-button>
        </a-form-item>
      </a-form>
      <div>{{ formConfig.userName }}----{{ formConfig.userPassword}}</div>
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
