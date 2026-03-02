<template>
  <h1>{{ message }}</h1>
  <img v-bind:src="imageUrl" alt="" />
  <br>
  <img :src="imageUrl" alt="" />

  <button @click=""changImg>Change image</button>
</template>

<script setup>
import {ref} from 'vue'
let message = 'Hello v-bind!'

let imageUrl='/public/img/banner_1.jpg'

function changImg(){
imageUrl.value='/public/img/banner_2.jpg'
}
</script>

<style scoped>
img {
  max-width: 300px;
}

.active {
  color: green;
}

.inactive {
  color: red;
  text-decoration: line-through;
}

.center {
  text-align: center;
}
</style>