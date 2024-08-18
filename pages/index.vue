<template>
  <div
    class="flex min-h-screen justify-center items-center bg-slate-100 dark:bg-slate-600"
  >
    <h1>Current mode: {{ $colorMode.value }}</h1>
  </div>
</template>

<script setup>
const colorMode = useColorMode();
</script>
