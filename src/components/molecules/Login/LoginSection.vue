
<script setup lang="ts">
import CBButton from "@/components/atoms/CBButton.vue";
import { ref } from 'vue';

const email = ref('');
const password = ref('');
const handleLogin = () => {
  console.log('Login attempt:', { email: email.value, password: password.value });
  alert('Login functionality to be implemented!');
};
</script>

<template>
  <div class="login-section">
    <h2 class="text-white text-xl mb-4">Sign in to your account</h2>

    <form @submit.prevent="handleLogin" class="space-y-4">
      <div>
        <label for="email" class="block text-white text-sm mb-1">Email address</label>
        <input
          v-model="email"
          type="email"
          id="email"
          required
          placeholder="Enter email"
          class="w-full p-2 bg-gray-800 text-white border border-gray-700 rounded-md focus:outline-none focus:border-blue-500"
        />
      </div>

      <div class="relative">
        <label for="password" class="block text-white text-sm mb-1">Password</label>
        <input
          v-model="password"
          type="password"
          id="password"
          required
          placeholder="Enter password"
          class="w-full p-2 bg-gray-800 text-white border border-gray-700 rounded-md focus:outline-none focus:border-blue-500"
        />
        <a href="#" class="absolute right-2 top-1/2 transform -translate-y-1/2 text-blue-500 text-sm hover:underline">Forgot password?</a>
      </div>

      <CBButton variant="blue" text="Sign in" />
    </form>

    <p class="mt-4 text-gray-400 text-sm">
      Not a member? <a href="#" class="text-blue-500 hover:underline">Start here</a>
    </p>
  </div>
</template>

<style scoped>
.login-section {
  padding: 20px;
  background-color: transparent; 
  width: 100%;
  max-width: 300px;
}
</style>
<style>

</style>