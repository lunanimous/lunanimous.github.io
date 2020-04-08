<template>
  <div>
    <Navbar />

    <div class="max-w-4xl mx-auto sm:flex items-center p-4 sm:p-6 my-16">
      <div class="m-8">
        <h2 class="text-4xl">Connect with the Nimiq blockchain</h2>
        <h3
          class="text-xl text-gray-600 mt-2"
        >Discover a suite of tools and projects to start using the Nimiq blockchain today</h3>
      </div>
      <div class="bg-white shadow-xl rounded-lg p-12">
        <img class="h-6" src="@/assets/images/nimiq-logo.svg" alt="nimiq" />
        <p class="text-lg mt-6">Barrier-free value exchange for everyone.</p>
        <a
          target="_blank"
          href="https://www.nimiq.com/"
          class="block font-bold mt-8 text-teal-500 hover:text-teal-600"
        >Visit nimiq.com</a>
      </div>
    </div>

    <section id="projects" class="bg-white my-8 px-4 sm:px-8 py-16">
      <div class="max-w-4xl mx-auto">
        <h3 class="text-center text-sm tracking-widest text-gray-500 uppercase">Projects</h3>
        <h4 class="text-center text-2xl mt-6">Useful tools and full fledge applications</h4>

        <div class="mt-8 flex flex-wrap -mx-4">
          <Project v-for="(project, i) in this.projects" :key="i" :project="project"></Project>
        </div>
      </div>
    </section>

    <section id="playground" class="my-8 px-4 sm:px-8 py-16">
      <div class="max-w-4xl mx-auto">
        <h3 class="text-center text-sm tracking-widest text-gray-500 uppercase">Playground</h3>
        <h4 class="text-center text-2xl mt-6">Crazy ideas, explorations and funny games</h4>

        <div class="mt-8 flex flex-wrap -mx-4">
          <Project
            v-for="(project, i) in this.playground"
            :key="i"
            :project="project"
            color="white"
          ></Project>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue';
import Project from '@/components/Project.vue';

export default {
  components: {
    Navbar,
    Project
  },
  data() {
    return {
      projects: [
        {
          name: 'Widgets',
          description: 'Accept NIM payment and donation on your website easily',
          link: 'https://lunanimous.github.io/nim-widgets/'
        },
        {
          name: 'Minim',
          description: 'Send and receive NIM directly from your mobile device',
          link: 'https://lunanimous.github.io/nim-widgets/'
        }
      ],
      playground: [
        {
          name: 'Tic Tac Toe',
          description: 'The famous game powered by NIM transactions',
          link: 'https://lunanimous.github.io/tic-tac-toe/'
        }
      ]
    };
  }
};
</script>
