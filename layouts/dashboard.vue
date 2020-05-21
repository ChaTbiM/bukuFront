<template>
  <v-app>
    <DashboardNavigation />
    <v-content>
      <v-container class="fill-height" fluid>
        <nuxt />
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import DashboardNavigation from '../components/DashboardNavigation'
export default {
  components: {
    DashboardNavigation
  },
  data() {
    return {}
  }
}
</script>

<style></style>
