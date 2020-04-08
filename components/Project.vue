<template>
  <div class="w-full sm:w-1/2 md:w-1/3 p-4">
    <div
      class="h-full rounded-lg p-6"
      :class="{ 'bg-white': this.color === 'white', 'bg-gray-100': this.color !== 'white' }"
    >
      <div
        class="h-12 w-12 rounded-full p-2 flex items-center justify-center"
        :class="{ 'bg-white': this.color !== 'white', 'bg-gray-100': this.color === 'white' }"
      >
        <slot>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="feather feather-package"
          >
            <line x1="16.5" y1="9.4" x2="7.5" y2="4.21" />
            <path
              d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"
            />
            <polyline points="3.27 6.96 12 12.01 20.73 6.96" />
            <line x1="12" y1="22.08" x2="12" y2="12" />
          </svg>
        </slot>
      </div>

      <h2 class="text-xl mt-4">{{this.project.name}}</h2>
      <p class="text-gray-600 mt-2">{{this.project.description}}</p>

      <a
        v-if="this.project.link"
        :href="this.project.link"
        target="_blank"
        class="inline-block mt-5 text-teal-500 hover:text-teal-600"
      >
        Go to
        <b class="font-bold">{{this.project.name}}</b>
      </a>
      <p
        v-if="!this.project.link"
        class="inline-block mt-4 py-2 px-3 bg-gray-300 text-gray-600 rounded-full text-sm"
      >Under construction...</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['project', 'color']
};
</script>
