<template>
  <div class="w-full sm:w-1/2 md:w-1/3 p-4">
    <div
      class="h-full rounded-lg p-6"
      :class="{ 'bg-white': this.color === 'white', 'bg-gray-100': this.color !== 'white' }"
    >
      <div
        class="h-12 w-12 rounded-full p-2 flex items-center justify-center text-teal-500"
        :class="{ 'bg-gray-200': this.color !== 'white', 'bg-gray-100': this.color === 'white' }"
      >
        <i v-bind:data-feather="this.project.icon"></i>
      </div>

      <h2 class="text-xl mt-4">{{this.project.name}}</h2>
      <p class="text-gray-600 mt-2">{{this.project.description}}</p>

      <a
        v-if="this.project.link"
        :href="this.project.link"
        target="_blank"
        class="inline-block mt-6 text-teal-500 hover:text-teal-600"
      >
        Go to
        <b class="font-bold">{{this.project.name}}</b>
      </a>
      <p
        v-if="!this.project.link"
        class="inline-block mt-6 py-1 px-3 bg-gray-200 text-gray-500 rounded-full text-sm"
      >Under construction...</p>
    </div>
  </div>
</template>

<script>
import feather from 'feather-icons';

export default {
  props: ['project', 'color'],
  mounted() {
    feather.replace();
  }
};
</script>
