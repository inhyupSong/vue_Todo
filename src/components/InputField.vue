<template>
  <div>
    <label for=""> Box for typing </label>
    <input
      type="text"
      :value="value"
      style="padding: 30px;"
      @input="$emit('input', $event.target.value)"
    />
  </div>
</template>

<script>
export default {
  props: {
    value: {
      type: String,
      required: true,
    },
  },
}
</script>
