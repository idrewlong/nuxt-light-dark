<template>
  <footer class="bg-slate-300 dark:bg-slate-600 py-12 px-4">
    <div
      aria-label="footer"
      class="focus:outline-none mx-auto container flex flex-col items-center justify-center"
    >
      <div aria-label="prodify logo" role="img">
        <NuxtLink to="/">
          <img src="#" alt="logo" class="h-16 hover:scale-105 duration-500" />
        </NuxtLink>
      </div>
      <div
        class="text-center md:text-left text-ivory flex flex-col md:items-center pt-3"
      >
        <div class="my-6 text-base text-ivory">
          <ul class="md:flex md:justify-center items-center uppercase">
            <li
              v-for="(link, index) in links"
              :key="index"
              class="md:mr-6 cursor-pointer pt-4 lg:py-0"
            >
              <NuxtLink
                :to="link.to"
                class="focus:outline-none text-ivory focus:underline hover:text-limegreen hover:underline duration-200 ease-in-out"
              >
                {{ link.text }}
              </NuxtLink>
            </li>
          </ul>
        </div>
        <div class="mb-6 flex justify-center space-x-4">
          <a
            v-for="(social, index) in socials"
            :key="index"
            :href="social.href"
            type="button"
            class="m-1 h-9 w-9 rounded-full border-2 border-white uppercase leading-normal text-white hover:text-limegreen hover:border-limegreen duration-200 ease-in-out"
            data-te-ripple-init
            data-te-ripple-color="light"
          >
            <span v-html="social.icon" class="mx-auto h-full w-4"></span>
          </a>
        </div>
      </div>
      <div class="w-9/12 h-0.5 bg-white rounded-full"></div>
      <div class="mt-6 text-sm text-ivory">
        <p class="focus:outline-none">
          © {{ new Date().getFullYear() }} All rights reserved
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup>
const links = [
  { to: "/about", text: "About" },
  { to: "/services", text: "Services" },
  { to: "/pricing", text: "Pricing" },
  { to: "/contact", text: "Contact" },
];

const socials = [
  {
    href: "#!",
    icon: '<svg xmlns="http://www.w3.org/2000/svg" class="mx-auto h-full w-4" fill="currentColor" viewBox="0 0 24 24"><path d="M9 8h-3v4h3v12h5v-12h3.642l.358-4h-4v-1.667c0-.955.192-1.333 1.115-1.333h2.885v-5h-3.808c-3.596 0-5.192 1.583-5.192 4.615v3.385z" /></svg>',
  },
  {
    href: "#!",
    icon: '<svg xmlns="http://www.w3.org/2000/svg" class="mx-auto h-full w-4" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z" /></svg>',
  },
  {
    href: "#!",
    icon: '<svg xmlns="http://www.w3.org/2000/svg" class="mx-auto h-full w-4" fill="currentColor" viewBox="0 0 24 24"><path d="M4.98 3.5c0 1.381-1.11 2.5-2.48 2.5s-2.48-1.119-2.48-2.5c0-1.38 1.11-2.5 2.48-2.5s2.48 1.12 2.48 2.5zm.02 4.5h-5v16h5v-16zm7.982 0h-4.968v16h4.969v-8.399c0-4.67 6.029-5.052 6.029 0v8.399h4.988v-10.131c0-7.88-8.922-7.593-11.018-3.714v-2.155z" /></svg>',
  },
  {
    href: "#!",
    icon: '<svg class="mx-auto h-full w-4" viewBox="0 -2.5 20 20" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" fill="#000000"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <defs> </defs> <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd"> <g id="Dribbble-Light-Preview" transform="translate(-300.000000, -922.000000)" fill="currentColor"> <g id="icons" transform="translate(56.000000, 160.000000)"> <path d="M262,764.291 L254,771.318 L246,764.281 L246,764 L262,764 L262,764.291 Z M246,775 L246,766.945 L254,773.98 L262,766.953 L262,775 L246,775 Z M244,777 L264,777 L264,762 L244,762 L244,777 Z" id="email-[#ffffff]"> </path> </g> </g> </g> </g></svg>',
  },
];
</script>
