<script setup>
import { ref } from 'vue';

const handleClick = () => {
  paras.value.push(newPara.value);
  newPara.value = '';
}
const paras = ref([])
const newPara = ref('');
const handleDelete = (i) => {
  paras.value.splice(i, 1);
}
</script>

<template>
  <div>
<input type="text" v-model="newPara" @keyup.enter="handleClick"></input>
</div>
<div>
  <h1>Paras</h1>
  <p @dblclick="handleDelete(i)" v-for="(text, i) in paras" :key="i">{{ text }}</p>
</div>
</template>
