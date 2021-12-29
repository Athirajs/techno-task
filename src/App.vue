<template>
  <div id="nav">
    <div class="nav-link">
      <router-link to="/">Home</router-link>
      <router-link to="/login">Login</router-link>
      <router-link to="/register">Register</router-link>
    </div>
  </div>
  <router-view />
</template>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

#nav {
  padding: 30px;
  background: rgb(13, 199, 91);
  height: 78px;
  .nav-link {
    margin-left: auto;
  }
  a {
    font-weight: bold;
    color: #ffffff;
    text-decoration: none;
    font-size: 20px;
    margin-left: 20px;

    &.router-link-exact-active {
      color: #d6f3e9;
    }
  }
}
</style>
