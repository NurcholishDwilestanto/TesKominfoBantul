<script setup>
import Vue from 'vue';
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
new Vue({
  el:'#app',
  data(){
    return{
      info:null
    }
  },
  mounted(){
    axios
    .get('http://192.168.2.99:8008')
    .then(response =>(this.info =response))
  }
})
</script>

<template>
  <main>
    <h1> FrondEnd</h1>
  </main>
  
  <span>{{info}}</span>
</template>

<style scoped>
</style>
