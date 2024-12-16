<template>
  <button :class="`btn ${size}`" @click="handleClick">
    {{ label }}
  </button>
</template>


<script setup>
import { defineProps, defineEmits } from 'vue';


const props = defineProps({
  label: {
    type: String,
    default: '按钮'
  },
  size: {
    type: String,
    default: 'default'
  }
});


const emit = defineEmits(['click']);


function handleClick() {
  emit('click');
}
</script>


<style>
.btn {
  padding: 10px;
  border: none;
  cursor: pointer;
}
.btn.large {
  font-size: 20px;
}
.btn.default {
  font-size: 16px;
}
.btn.small {
  font-size: 12px;
}
</style>
