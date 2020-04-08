<template>
  <div
    class="fixed z-10 w-full top-0 sm:flex items-center justify-between p-4 pb-16 sm:pb-6 navbar"
  >
    <div class="justify-center sm:justify-right mb-2">
      <a href="/" class="block">
        <img class="h-10 mx-auto" src="@/assets/images/lunanimous-logo.svg" alt="lunanimous" />
      </a>
    </div>
    <div class="flex justify-center sm:justify-right">
      <a class="block py-2 px-4 text-gray-600 hover:text-gray-800" href="#projects">Projects</a>
      <a class="block py-2 px-4 text-gray-600 hover:text-gray-800" href="#playground">Playground</a>
      <a
        class="block py-2 px-4 text-gray-400"
        href="#blog"
        aria-label="Coming soon..."
        data-microtip-position="bottom-left"
        role="tooltip"
      >Blog</a>
      <a
        class="block py-2 px-4 text-gray-600 hover:text-gray-800"
        target="_blank"
        href="https://github.com/lunanimous"
        aria-label="Github"
        data-microtip-position="bottom-left"
        role="tooltip"
      >
        <i data-feather="github"></i>
      </a>
    </div>
  </div>
</template>

<script>
import feather from 'feather-icons';

export default {
  mounted() {
    feather.replace();
  }
};
</script>

<style>
.navbar {
  background: linear-gradient(
    #f7f8f8 0%,
    rgba(247, 248, 248, 70) 50%,
    rgba(247, 248, 248, 0) 100%
  );
}
</style>
