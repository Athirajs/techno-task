<template>
  <div class="main">
    <SidePanel />
    <HomeContent />
  </div>
</template>
<script>
import SidePanel from "../views/SidePanel.vue";
import HomeContent from "./HomeContent.vue";
export default {
  components: {
    SidePanel,
    HomeContent,
  },
};
</script>
<style lang="scss" scoped>
.main {
  display: flex;
}
</style>
