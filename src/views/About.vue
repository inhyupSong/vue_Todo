<template>
  <div>
    <div class="mx-auto" style="width: 300px;">
      <h1>About Page</h1>
      <!--     <SongsPractice siteTitle="Songs page" siteName="About site" />
 -->
      <InputField v-model="textField" />
      <button @click="updateName">Submit</button>

      {{ textField }}
    </div>
  </div>
</template>

<script>
/* import SongsPractice from '@/components/SongsPractice.vue' */
import InputField from '@/components/InputField.vue'
export default {
  data() {
    return {
      textField: 'Gätzibrunnenstrasse 10',
    }
  },

  components: {
    /* SongsPractice, */
    InputField,
  },

  methods: {
    updateName() {
      this.textField = 'Winterthur'
    },
  },

  beforeCreate() {
    console.log('beforeCreate alert', this.name)
  },
  created() {
    console.log('created alert', this.name)
  },
  /*   beforeMount() {
    alert('beforeMount alert', this.name)
  },
  mounted() {
    alert('mounted alert', this.name)
  }, */
  updated() {
    alert('updated alert', this.name)
  },
  beforeDestroy() {
    console.log('beforeDestroy alert', this.name)
  },
  destroyed() {
    console.log('destroyed alert', this.name)
  },
}
</script>
