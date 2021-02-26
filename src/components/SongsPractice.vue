<template>
  <div>
    <h1 v-if="show">Yes. it is shown</h1>
    <h1 :class="{ red: isRed }">{{ text_red }}</h1>
    <!--     <h1 v-if="text_red">it will be red.</h1>
 -->
    <button @click="update">click</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text_red: 'it will be red',
      show: true,
      isRed: false,
    };
  },
  methods: {
    update() {
      this.show = !this.show;
      this.isRed = !this.isRed;
      this.text_red = 'it is red';
    },
  },
};
</script>

<style scoped>
.red {
  color: red;
}
</style>
/* */ /* */
