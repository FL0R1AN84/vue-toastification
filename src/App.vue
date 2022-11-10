<script setup lang="ts">
import { useToast } from 'vue-toastification';
const toast = useToast();

const info = () => toast.info('You did it! 🎉');
const success = () => toast.success('You did it! 🎉');
const warning = () => toast.warning('You did it! 🎉');
const error = () => toast.error('You did it! 🎉');
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
}

.btn-green {
  @include button-bg(#3d8b3f);
}

.btn-blue {
  @include button-bg(#3498db);
}

.btn-yellow {
  @include button-bg(#967000);
}

.btn-red {
  @include button-bg(#9b0001);
}
</style>
