<template>
  <div class="font-sans text-teal-900 pt-20">
    <Navbar />
    <nuxt />
    <Footer />
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue';
import Footer from '@/components/Footer.vue';

export default {
  components: { Navbar, Footer }
};
</script>

<style>
body {
  background: #f7f8f8;
}
</style>
