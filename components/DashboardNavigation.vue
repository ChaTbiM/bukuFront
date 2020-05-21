<template>
  <!-- navigation  -->
  <v-navigation-drawer app right absolute dark>
    <v-list dense nav class="py-0">
      <!-- <v-list-item two-line :class="miniVariant && 'px-0'">
        <v-list-item-avatar>
          <img src="https://randomuser.me/api/portraits/men/81.jpg" />
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>Application</v-list-item-title>
          <v-list-item-subtitle>Subtext</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item> -->

      <v-list-item>
        <v-list-item-content>
          <h1 class="display-2 text-center">بوكو</h1>
        </v-list-item-content>
      </v-list-item>
      <v-divider></v-divider>
    </v-list>

    <v-list>
      <v-list-item-group v-model="item" color="primary">
        <v-list-item v-for="(item, i) in items" :key="i" :to="item.link">
          <v-list-item-content>
            <v-list-item-title
              color="text--white"
              v-html="item.title"
            ></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-navigation-drawer>
  <!-- / -->
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: 'الكتب المتوفرة', link: '/exchange' },
        { title: 'أودع كتاب', link: '/deposit' }
      ]
    }
  }
}
</script>

<style></style>
