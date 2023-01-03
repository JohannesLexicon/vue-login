<template>
  <TheNavbar
    :user="user"
    @show-login="showLogin = true"
    @logout="user = ''"
  />
  <main class="main">
    <SignInForm
      v-if="showLogin"
      @login="handleLogin"
    />
    <Home
      v-else
      :user="user"
    />
  </main>
</template>

<script setup>
import { ref } from 'vue';
import TheNavbar from './components/TheNavbar.vue';
import Home from './components/Home.vue';
import SignInForm from './components/SignInForm.vue';

const showLogin = ref(false);
const user = ref('');

const handleLogin = (_user) => {
  user.value = _user;
  showLogin.value = false;
};
</script>

<style scoped>
.main {
  padding: 8px;
}
</style>
