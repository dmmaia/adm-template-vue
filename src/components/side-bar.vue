<template>
  <div class="side-bar">
    <div class="sub-menu">
      <h3>ADM template</h3>
    </div>
    <div class="sub-menu">
      <div class="menu-button">Dashboard</div>
    </div>
    <div class="sub-menu">
      <div v-for="item in menus" :key="item.path">
        <div class="menu-button">{{ item.page }}</div>
      </div>
    </div>
    <button class="hide-button"><</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  setup() {
    return {
      menus: [
        {
          page: 'page1',
          path: '/'
        },
        {
          page: 'page2',
          path: '/'
        }
      ]
    }
  }
})
</script>

<style scoped>
.hide-button {
  background-color: rgb(95, 95, 252);
  border: 0;
  font-size: 20px;
  width: 5vh;
  height: 5vh;
  border-radius: 3vh;
  color: white;
  position: fixed;
  bottom: 2vh;
  left: 13%;
}
.side-bar p {
  color: rgba(255, 255, 255, 0.699);
}
.menu-button {
  margin-top: 2vh;
  margin-bottom: 2vh;
}
.side-bar .sub-menu {
  width: 80%;
  border-bottom: rgba(255, 255, 255, 0.466) 0.5px solid;
  margin-left: auto;
  margin-right: auto;
}
.side-bar {
  color: white;
  position: fixed;
  width: 15%;
  height: 100%;
  background-color: #395fd1;
}
</style>
