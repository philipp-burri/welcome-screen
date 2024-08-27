<script setup> 
import { ref } from 'vue';

const cardTitle = ref('Welcome to Opportunity')

let date = new Date(Date.UTC(2012, 11, 20, 3, 0, 0));
let options = { /* weekday: 'long',  */ year: 'numeric', month: 'numeric', day: 'numeric' };
</script>

<template>
    <div class="cardTitle">{{ cardTitle }}</div>
    <div class="date">{{ new Date().toLocaleString("de-ch", options) }}</div>
</template>

<style scoped>
.cardTitle{
  padding-top: 70px;
  font-size: 62px;
  font-weight: 900;
  color: #323D4A;
}
.date{
  margin-top: 21px;
  font-size: 62px;
  font-weight: 500;
  color: #9AA7B1;
}
</style>