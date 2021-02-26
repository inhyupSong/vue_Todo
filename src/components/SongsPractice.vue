<template>
  <div>
    <!--         <h1 v-if="show">Yes. it is shown</h1>
    <h1 :class="{ red: isRed }">{{ text_red }}</h1>
    <button @click="update">click</button> -->
    <h2>{{ siteTitle }}</h2>
    <h2>{{ siteName }}</h2>
  </div>
</template>

<script>
export default {
  props: {
    siteTitle: {
      type: String,
      default: 'default title',
    },
    siteName: {
      type: String,
      default: 'site default name',
    },
  },
  data() {
    return {
      text_red: 'it will be red',
      show: true,
      isRed: false,
    }
  },
  methods: {
    update() {
      this.show = !this.show
      this.isRed = !this.isRed
      this.text_red = 'it is red'
    },
  },
}
</script>

<style scoped>
.red {
  color: red;
}
</style>
/* */ /* */
