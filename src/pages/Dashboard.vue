<template>
  <div class="flex min-h-screen w-screen bg-gray-100 text-gray-900">
    <!-- Sidebar -->
    <aside class="w-60 bg-white p-5 shadow-md">
      <div class="mb-10">
        <h2 class="text-xl font-bold text-blue-600">Dashboard</h2>
      </div>

      <nav class="space-y-3">
        <a
          href="#"
          class="block px-3 py-2 rounded hover:bg-blue-100 font-medium"
          >🏠 Home</a
        >
        <a
          href="#"
          class="block px-3 py-2 rounded bg-blue-100 text-blue-600 font-medium"
          >📊 Overview</a
        >
        <a
          href="#"
          class="block px-3 py-2 rounded hover:bg-blue-100 font-medium"
          >🧑 Users</a
        >
        <a
          href="#"
          class="block px-3 py-2 rounded hover:bg-blue-100 font-medium"
          >⚙️ Settings</a
        >
      </nav>

      <div class="mt-10">
        <button
          class="w-full bg-blue-600 text-white py-2 rounded hover:bg-blue-700 text-sm"
        >
          Upgrade Plan
        </button>
      </div>
    </aside>

    <!-- Main Content -->
    <main class="flex-1 p-6">
      <!-- Top Header -->
      <div class="flex justify-between items-center mb-6">
        <h1 class="text-2xl font-bold">Welcome Back, Justin!</h1>
        <div class="text-sm text-gray-500">Today: {{ currentDate }}</div>
      </div>

      <!-- Info Cards -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
        <div class="bg-white p-4 rounded-lg shadow-md">
          <p class="text-gray-500 text-sm mb-1">Total Users</p>
          <p class="text-2xl font-bold">{{ stats.users }}</p>
        </div>
        <div class="bg-white p-4 rounded-lg shadow-md">
          <p class="text-gray-500 text-sm mb-1">New Signups</p>
          <p class="text-2xl font-bold">{{ stats.signups }}</p>
        </div>
        <div class="bg-white p-4 rounded-lg shadow-md">
          <p class="text-gray-500 text-sm mb-1">Active Sessions</p>
          <p class="text-2xl font-bold">{{ stats.sessions }}</p>
        </div>
        <div class="bg-white p-4 rounded-lg shadow-md">
          <p class="text-gray-500 text-sm mb-1">Revenue</p>
          <p class="text-2xl font-bold">
            ${{ stats.revenue.toLocaleString() }}
          </p>
        </div>
      </div>
    </main>
  </div>
</template>

<script setup>
const currentDate = new Date().toLocaleDateString(undefined, {
  weekday: "long",
  month: "short",
  day: "numeric",
  year: "numeric",
});

const stats = {
  users: 12840,
  signups: 423,
  sessions: 985,
  revenue: 23450,
};
</script>

<style scoped>
body {
  font-family: "Inter", sans-serif;
}
</style>
