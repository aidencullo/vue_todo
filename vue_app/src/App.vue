<script setup>
const handleClick = () => {
  paras.push('This is the fourth paragraph');
}
const paras = []
</script>

<template>
  <div>
<button @click="handleClick">Click me</button>
</div>
<div>
  <p v-for="(text, i) in paras" :key="i">{{ text }}</p>
</div>
</template>
