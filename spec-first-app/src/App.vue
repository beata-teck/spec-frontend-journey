<script setup>
import {ref} from 'vue';
const name = ref('');      
</script> 

<template>
  <div>
    
    <h2>Enter Your Name</h2>
    <input v-model="name" placeholder="write Ur name"/>
    <h2 v-if="name !== ''">Hello {{ name }}!</h2>


    
  </div>
</template>


<style scoped>
  h2 {
    color: #42b983;
  }
</style>

