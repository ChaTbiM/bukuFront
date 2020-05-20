<template>
  <v-layout>
    <p>Exchanges <span v-text="id"></span></p>
  </v-layout>
</template>

<script>
export default {
  layout: 'dashboard',
  data() {
    return {
      id: this.$route.params.id
    }
  }
}
</script>
