<script setup>
import { ref } from 'vue';

const handleClick = () => {
  paras.value.push(newPara.value);
  newPara.value = '';
}
const paras = ref([])
const newPara = ref('');
</script>

<template>
  <div>
<input type="text" v-model="newPara" @keyup.enter="handleClick"></input>
</div>
<div>
  <h1>Paras</h1>
  <p v-for="(text, i) in paras" :key="i">{{ text }}</p>
</div>
</template>
