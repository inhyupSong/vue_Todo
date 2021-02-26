<template>
  <div id="app">
    <TopMenu />
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
import TopMenu from './components/layout/TopMenu.vue'

export default {
  name: 'app',
  components: {
    TopMenu,
  },
}
</script>

<style></style>
