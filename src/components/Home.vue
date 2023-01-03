<template>
  <main>
    <span v-if="user">Welcome {{ user }}!</span>
    <span v-else>Please login!</span>
  </main>
</template>

<script setup>
defineProps(['user']);
</script>
