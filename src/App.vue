<script setup lang="ts">
import { useToast } from 'vue-toastification';
const toast = useToast();

const info = () => toast.info('Information 🤔');
const success = () => toast.success('Success 😉');
const warning = () => toast.warning('Warning 😫');
const error = () => toast.error('Error 🤪');
</script>

<template>
  <div>
    <button class="btn btn-blue" @click="info">Show info</button>
    <button class="btn btn-green" @click="success">Show success</button>
    <button class="btn btn-yellow" @click="warning">Show warning</button>
    <button class="btn btn-red" @click="error">Show error</button>
  </div>
</template>

<style lang="scss" scoped>
@mixin button-bg($bg) {
  background: $bg;
  &:hover {
    background: darken($bg, 8%);
    transition: all 0.3s ease;
  }
  &:active {
    background: darken($bg, 25%);
  }
}

.btn {
  color: white;
  text-decoration: none;
  padding: 5px 10px;
  border-radius: 3px;
  font-family: 'Poiret One', cursive;
  font-size: 2em;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.btn-green {
  @include button-bg(#4caf51);
}

.btn-blue {
  @include button-bg(#2196f3);
}

.btn-yellow {
  @include button-bg(#ffc108);
}

.btn-red {
  @include button-bg(#ff5253);
}
</style>
