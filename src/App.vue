<template>
  <div class="app">
    <Sidebar>
      <template v-slot:sidebar>
        <h1>Sidebar</h1>
      </template>
      <template v-slot:not-sidebar>
        <h1>NotSidebar</h1>
      </template>
    </Sidebar>
  </div>
</template>

<script>
import Sidebar from "./components/Sidebar.vue";
export default {
  components: {
    Sidebar,
  },
};
</script>

<style scoped>
.app {
  width: 100vw;
  height: 100vh;
}
</style>
