<!-- src/LoginView.vue -->
<script setup lang="ts">
import { ref } from 'vue'
import router from "@/router";
import { useRoute } from "vue-router";
import LoginSection from "@/components/molecules/Login/LoginSection.vue"
</script>

<template>
  <main class="h-screen w-screen flex items-center justify-center bg-black">
    <div class="text-center">
      <img src="@/assets/logo.png" alt="Logo" class="mx-auto mb-6" style="width: 60px;" />
      <LoginSection />
    </div>
  </main>
</template>
