<template>
  <div>
    <p>Kopf</p>
    <slot name="kopf" :exportText="givenText"></slot>

    <p>Koeper</p>
    <slot></slot>
    <!-- Default slot -->

    <p>fuss</p>
    <slot></slot>
    <!-- Default slot -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      givenText: 'Abla Katabla',
    }
  },
}
</script>
