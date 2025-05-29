<template>
  <div class="flex items-center justify-center">
    <div
      class="w-[400px] h-[290px] bg-white/80 backdrop-blur-md rounded-2xl shadow-2xl p-10 border border-emerald-100 flex flex-col justify-center"
    >
      <h2
        class="text-3xl font-extrabold mb-6 text-center text-emerald-700 tracking-tight"
      >
        Sign In
      </h2>
      <form @submit.prevent="login" class="flex flex-col gap-4">
        <div>
          <label class="block text-emerald-700 font-medium mb-1" for="email"
            >Email</label
          >
          <input
            v-model="email"
            type="email"
            id="email"
            class="w-full px-3 py-1.5 border border-emerald-200 rounded-lg focus:outline-none focus:ring-2 focus:ring-emerald-400 bg-emerald-50 placeholder-emerald-300 transition"
            placeholder="you@example.com"
            required
          />
        </div>
        <div>
          <label class="block text-emerald-700 font-medium mb-1" for="password"
            >Password</label
          >
          <input
            v-model="password"
            type="password"
            id="password"
            class="w-full px-3 py-1.5 border border-emerald-200 rounded-lg focus:outline-none focus:ring-2 focus:ring-emerald-400 bg-emerald-50 placeholder-emerald-300 transition"
            placeholder="••••••••"
            required
          />
        </div>
        <button
          type="submit"
          class="w-full bg-gradient-to-r from-emerald-500 to-green-500 text-white py-2 rounded-lg font-semibold shadow-md hover:from-emerald-600 hover:to-green-600 transition"
        >
          Login
        </button>
      </form>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const email = ref("");
const password = ref("");

function login() {
  console.log("Email:", email.value);
  console.log("Password:", password.value);
}
</script>

<style scoped></style>
