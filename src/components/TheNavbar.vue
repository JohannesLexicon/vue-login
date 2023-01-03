<template>
  <nav class="navbar">
    <span>nav</span>
    <!-- Om det finns en user visar vi den och ger möjligheten att logga ut -->
    <div v-if="user">
      <span>{{ user }}</span>
      <button @click="$emit('logout')">Logout</button>
    </div>
    <!-- Annars ger vi möjlighet att logga in -->
    <div v-else>
      <button @click="$emit('show-login')">Login</button>
    </div>
  </nav>
</template>

<script setup>
defineProps(['user']);
</script>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  background-color: aliceblue;
  padding: 8px;
}
</style>
