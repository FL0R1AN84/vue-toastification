<script setup lang="ts">
import { useToast } from "vue-toastification";
const toast = useToast();

const success = () => toast.success("You did it! 🎉");
</script>

<template>
  <div class="grid grid-cols-1">
    <div>
      <button class="" @click="success">Show success</button>
    </div>
  </div>
</template>

<style scoped></style>
