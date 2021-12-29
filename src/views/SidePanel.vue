<template>
  <div class="sidebar">
    <div class="sidemenu">
      <div class="menu">
        <p>Company Link</p>
      </div>
      <div class="menu">
        <p>Company Link</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.sidebar {
  background: #fafafa;
  width: 25%;
  height: calc(100vh - 78px);
  //   min-height: 200px;
  overflow: auto;
  position: -webkit-sticky;
  position: sticky;
  //  top: 5%;

  .sidemenu {
    .menu {
      border-bottom: 1px solid #333;
      padding: 20px;
      p {
        font-size: 18px;
        font-weight: bold;
      }
    }
  }
}
</style>
