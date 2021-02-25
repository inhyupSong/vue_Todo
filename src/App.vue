<template>
  <div id="app">
    <Header />
    <div id="content" class="content">
      <div>
        <!--    <router-link to="/">Home </router-link>
        <router-link to="/about"> About </router-link> -->
        <router-view />
      </div>
    </div>
  </div>
</template>

<script>
import Header from './components/layout/Header.vue';

export default {
  name: 'app',
  components: {
    Header,
  },
};
</script>

<style></style>
