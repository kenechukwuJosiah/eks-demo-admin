<script setup>
import HelloWorld from "../components/HelloWorld.vue";
import Login from "../components/Login.vue";
import TheWelcome from "../components/TheWelcome.vue";
</script>

<template>
  <header>
    <div class="wrapper w-full space-y-3">
      <HelloWorld msg="Welcome to Admin Service!" />
      <div class="h-4"></div>
      <Login />
    </div>
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
  }
}
</style>
