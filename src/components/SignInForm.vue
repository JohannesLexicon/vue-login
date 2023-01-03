<template>
  <!-- $event.target är vad som skapade eventet. I den letar vi efter
  ett fält som heter (name) user och emittar värdet på detta -->
  <form @submit.prevent="$emit('login', $event.target.user.value)">
    <label for="user">user</label>
    <input
      type="text"
      id="user"
      name="user"
      required
    />
    <button>Submit</button>
  </form>
</template>

<script setup></script>
