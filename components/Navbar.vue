<template>
  <nav class="bg-purple-400">
    <div class="max-w-6xl mx-auto px-4">
      <div class="flex justify-between">

        <div class="flex space-x-4">
          <!-- logo -->
          <div>
            <nuxt-link to="/" no-prefetch class="flex items-center py-5 px-2 text-gray-700 hover:text-gray-900">
              <span class="font-bold">hornsandhooves</span>
            </nuxt-link>
          </div>

          <!-- primary nav 
          <div class="hidden md:flex items-center space-x-1">
            <a href="#" class="py-5 px-3 text-gray-700 hover:text-gray-900">Features</a>
            <a href="#" class="py-5 px-3 text-gray-700 hover:text-gray-900">Pricing</a>
          </div>
          -->
        </div>

        <!-- secondary nav -->
        <div class="hidden md:flex items-center space-x-1">
          <nuxt-link to="/about" class="py-2 px-3 hover:text-gray-900 text-gray-700 rounded transition duration-300">
            About
          </nuxt-link>
          <nuxt-link to="/contacts" class="py-2 px-3 hover:text-gray-900 text-gray-700 rounded transition duration-300">
            Contacts
          </nuxt-link>
          <nuxt-link to="/users" class="py-2 px-3 hover:text-gray-900 text-gray-700 rounded transition duration-300">
            Users
          </nuxt-link>
          <nuxt-link to="/login" class="py-2 px-3 hover:text-gray-900 text-gray-700 rounded transition duration-300">
            Login
          </nuxt-link>
        </div>

        <!-- mobile button goes here -->
        <div class="md:hidden flex items-center">
          <button class="mobile-menu-button">
            <svg class="w-6 h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
          </button>
        </div>

      </div>
    </div>

    <!-- mobile menu -->
    <div class="mobile-menu hidden md:hidden">
      <nuxt-link to="/about" class="block text-center py-2 px-4 text-sm text-gray-700 hover:text-gray-300 hover:bg-purple-600">
        About
      </nuxt-link>
      <nuxt-link to="/contacts" class="block text-center py-2 px-4 text-sm text-gray-700 hover:text-gray-300 hover:bg-purple-600">
        Contacts
      </nuxt-link>
      <nuxt-link to="/users" class="block text-center py-2 px-4 text-sm text-gray-700 hover:text-gray-300 hover:bg-purple-600">
        Users
      </nuxt-link>
      <nuxt-link to="/login" class="block text-center py-2 px-4 text-sm text-gray-700 hover:text-gray-300 hover:bg-purple-600">
        Login
      </nuxt-link>
    </div>
  </nav>
</template>

<script>

export default {
  mounted() {
    const btn = document.querySelector("button.mobile-menu-button");
    const menu = document.querySelector(".mobile-menu");

    // add event listeners
    btn.addEventListener("click", () => {
      menu.classList.toggle("hidden");
});
  }
}
</script>

<style>
/* active nav buttons */

.nuxt-link-active {
  @apply font-bold
}

/* custom non-Tailwind CSS */

@media (max-width: 576px) {
    .content {
        padding-top: 51px;
    }
}

@media (min-width: 577px) {
  .pt-scroll {
    padding-top: 51px;
  }

  .nav-sticky {
    position: fixed!important;
    min-width: 100%;
    top: 0;
    box-shadow: 0 2px 4px 0 rgba(0, 0, 0, .1);
    transition: all .25s ease-in;
    z-index: 1;
  }
}

/* HAMBURGER MENU */

.hamburger {
  cursor: pointer;
  width: 48px;
  height: 48px;
  transition: all 0.25s;
}
 
.hamburger__top-bun,
.hamburger__bottom-bun {
  content: '';
  position: absolute;
  width: 24px;
  height: 2px;
  background: #000;
  transform: rotate(0);
  transition: all 0.5s;
}

.hamburger:hover [class*="-bun"] {
  background: #333;
}

.hamburger__top-bun {
  transform: translateY(-5px);
}

.hamburger__bottom-bun {
  transform: translateY(3px);
}

.open {
  transform: rotate(90deg);
  transform: translateY(-1px);
}

.open .hamburger__top-bun {
  transform:
    rotate(45deg)
    translateY(0px);
}

.open .hamburger__bottom-bun {
  transform:
    rotate(-45deg)
    translateY(0px);
}
</style>