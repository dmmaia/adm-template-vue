<template>
  <div class="main-container">
    <SideBar />
    <div class="content">
      <Dashboard/>
    </div>
  </div>
</template>

<script setup>
import SideBar from './side-bar.vue'
import Dashboard from '../pages/dashboard.vue'
</script>

<style scoped>
.content {
  width: 75%;
  padding-left: 15%;
  height: 100%;
}
.main-container {
  display: flex;
  height: 100vh;
  overflow: scroll;
  background-color: rgba(0, 0, 255, 0.08);
}
</style>
