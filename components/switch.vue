<template>
  <button
    class="relative inline-flex items-center h-6 rounded-full w-11 focus:outline-none"
    :class="$colorMode.value === 'dark' ? 'bg-slate-900' : 'bg-gray-200'"
    @click="toggleColorMode"
  >
    <span
      class="inline-block w-4 h-4 transform transition ease-in-out duration-200 rounded-full bg-white shadow"
      :class="$colorMode.value === 'dark' ? 'translate-x-6' : 'translate-x-1'"
    ></span>
  </button>
</template>

<script setup>
const colorMode = useColorMode();

const toggleColorMode = () => {
  colorMode.preference = colorMode.value === "dark" ? "light" : "dark";
};
</script>
