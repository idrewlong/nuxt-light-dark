<template>
  <div class="bg-slate-100 dark:bg-slate-600 py-4 px-2">
    <nav
      class="bg-slate-100 dark:bg-slate-600 text-black dark:text-white max-w-7xl container sm:rounded-3xl px-10 py-4 mx-auto md:flex md:justify-between md:items-center"
    >
      <div class="flex items-center justify-between">
        <NuxtLink to="/" class="flex items-center">
          <img src="#" class="h-14 hover:scale-105 duration-200" alt="" />
          <span
            class="text-2xl font-semibold whitespace-nowrap text-white"
          ></span>
        </NuxtLink>
        <!-- Mobile menu button -->
        <div class="flex md:hidden">
          <button
            type="button"
            class="hover:text-gray focus:outline-none focus:text-gray-400"
            aria-label="Toggle Navigation"
            @click="toggleNavbar"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="white"
              class="w-6 h-6"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
              />
            </svg>
          </button>
        </div>
      </div>
      <!-- Mobile Menu open: "flex", Menu closed: "hidden" -->
      <div
        :class="[
          'flex-col mt-8 space-y-4 md:flex md:space-y-0 md:flex-row md:items-center md:space-x-10 md:mt-0 uppercase',
          showMenu ? 'flex' : 'hidden',
        ]"
      >
        <NuxtLink
          class="duration-500 hover:text-electriclime hover:underline ease-in-out"
          to="/about"
          @click="closeNavbar"
          >About</NuxtLink
        >
        <NuxtLink
          class="duration-500 hover:text-electriclime hover:underline ease-in-out"
          to="/services"
          @click="closeNavbar"
          >Services</NuxtLink
        >
        <NuxtLink
          class="duration-500 hover:text-electriclime hover:underline ease-in-out"
          to="/pricing"
          @click="closeNavbar"
          >Pricing</NuxtLink
        >
        <!-- <NuxtLink
                  class="text-ivory duration-500 hover:text-electriclime hover:underline ease-in-out"
                  to="/contact"
                  @click="closeNavbar"
                  >Contact</NuxtLink
                > -->
        <NuxtLink
          class="duration-500 hover:text-electriclime hover:underline ease-in-out"
          to="/contact"
          @click="closeNavbar"
          >Contact</NuxtLink
        >
        <!-- Contact button for medium screens and higher -->
        <Switch />
      </div>
    </nav>
  </div>
</template>

<script setup>
const showMenu = ref(false);

function toggleNavbar() {
  showMenu.value = !showMenu.value;
}

function closeNavbar() {
  showMenu.value = false;
}

const colorMode = useColorMode();

console.log(colorMode.preference);
</script>
