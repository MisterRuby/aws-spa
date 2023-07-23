<script setup lang="ts">
import axios from "axios";

const onclickButton = () => {
  alert("API 요청!")
  axios.post('http://localhost:8080')
    .then(res => {
      alert("API 요청 완료!")
    })
    .catch(e => {
      alert("API 요청 실패!")
    })
}

</script>

<template>
  <div class="container">
    <div>Web Server URL : localhost:5173</div>
    <div>API Server URL : localhost:8080</div>
    <button @click="onclickButton">API 요청</button>
  </div>
</template>

<style>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

button {
  border : none;
  background-color: deepskyblue;
  color: white;
  width: 100px;
  height: 30px;
  font-size: 16px;
}
</style>