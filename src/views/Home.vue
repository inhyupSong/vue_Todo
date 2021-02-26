<template>
  <div>
    <div class="mx-auto" style="width: 300px;">
      <h1>Welcome home</h1>
      <SongsPractice siteTitle="Songs page" siteName="About site" />
      <form action="">
        <InputField v-model="textField" /> <br />
        <button>Submit</button>
      </form>
      <p>{{ textField }}</p>

      <slot-practice>
        <template #kopf="{ exportText }">
          <p>between Kopf and Koeper + {{ exportText }}</p>
        </template>

        <template #default>
          <p>Default slot</p>
        </template>
      </slot-practice>
    </div>
  </div>
</template>

<script>
import SongsPractice from '@/components/SongsPractice.vue'
import InputField from '@/components/InputField.vue'
import SlotPractice from '@/components/SlotPractice.vue'

export default {
  components: {
    SongsPractice,
    InputField,
    SlotPractice,
  },
  data() {
    return {
      textField: '',
    }
  },
}
</script>

<style scoped>
h1 {
  color: blue;
}
</style>
