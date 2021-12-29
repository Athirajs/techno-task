<template>
  <div class="container">
    <h2>Login</h2>
    <form class="form-login">
      <div>
        <div class="input">
          <input type="text" placeholder="Username" v-model="username" />
        </div>
        <div class="input">
          <input type="password" placeholder="Password" v-model="password" />
        </div>
      </div>
      <div class="login-button">
        <button class="button" @click.prevent="login"><b>Log In</b></button>
      </div>
    </form>
  </div>
</template>
<script>
export default {
  data() {
    return {
      username: "",
      password: "",
    };
  },
};
</script>
<style scoped>
.container {
  margin: 100px auto;
  text-align: center;
  width: 396px;

  background: #fff;
  border-radius: 8px;
  float: none;
  color: #1c1e21;
  padding-bottom: 24px;
  padding-top: 10px;
  box-shadow: 0 2px 4px rgb(0 0 0 / 10%), 0 8px 16px rgb(0 0 0 / 10%);
}
.form-login {
  margin: 0;
  padding: 0;
  display: block;
}

input {
  background: #fff;
  color: #1c1e21;
  font-size: 17px;
  padding: 14px 16px;
  width: 330px;
  border-radius: 6px;
  background: #ffffff;
  border: 1px solid #dddfe2;
  color: #1d2129;
  margin-top: 16px;
}
.button {
  background: rgb(13, 199, 91);
  border: none;
  border-radius: 6px;
  font-size: 22px;
  line-height: 48px;
  padding: 0 16px;
  width: 364px;
  cursor: pointer;
  display: inline-block;
  text-decoration: none;
  white-space: nowrap;
  color: #fff;
  margin-top: 16px;
}
</style>
