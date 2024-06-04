<template>
  <div>
    <div class="title">Dashboard</div>
    <div class="container">
    <div v-for="(item, index) in cards" :key="index" class="card">
      <div class="card-content">
        <div class="name">{{item.name}}</div>
        <div class="content">{{item.value}}</div>
      </div>
      <div class="icon">$</div>
    </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    setup(){
      return{
        cards:[
          {
            name: "users",
            value: 100
          },
          {
            name: "posts",
            value: 50
          },
          {
            name: "renevue",
            value: "$500,00"
          },
        {
            name: "posts",
            value: 50
          },
        ]
      }
    }
  })
</script>

<style scoped>
.container{
  display: flex;
  justify-content: center;
  color: gray;
}
.title{
  font-size: 22px;
  margin-left: 1vw;
  color: gray;
  margin-top: 4vh;
  margin-bottom: 4vh;
}
.card .name {
  color: #395fd1;
  font-size: 15px;
  text-transform: uppercase;
}
.card .content{
 font-size: 20px;
  font-weight: bold;
}
.card .icon{
  font-size: 35px;
  color: rgba(0,0,0,0.2);
  font-weight: bold;
}
.card-content{

}
.card{
  align-items: center;
  justify-content: space-between;
  display: flex;
  margin-top: 1vw;
  width: 15vw;
  border-radius: 0.5vw;
  margin-left: 1vw;
  margin-right: 1vw;
  background-color: white;
  padding: 25px 20px 25px 20px;
  border-left: #395fd1 5px solid; 
}
</style>
