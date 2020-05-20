<template>
  <v-layout>
    <v-row align="center" justify="center">
      <v-col cols="12" sm="8" md="4">
        <v-card>
          <v-toolbar color="secondary" dark flat> </v-toolbar>
          <v-card-text>
            <v-form ref="form">
              <v-text-field label="إسم الكتاب" required></v-text-field>
              <v-text-field label="إسم الكاتب" required></v-text-field>
              <v-text-field label="سنة النشر"></v-text-field>
              <v-text-field
                label="الرقم العالمي الموحد للكتاب (isbn)"
              ></v-text-field>

              <!-- submit book btn -->
              <v-btn large color="primary" @click="submitBook"
                >أودع الكتاب</v-btn
              >
            </v-form>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-layout>
</template>

<script>
export default {
  layout: 'dashboard',
  data() {
    return {
      exchangeType: null,
      items: ['أي كتاب من تصنيف معين', 'أي كتاب من أي تصنيف', 'كتاب محدد'],
      categories: ['خيال', 'سيرة ذاتية', 'رياضيات', 'أعمال', 'أطفال']
    }
  },
  requestBook() {
    console.log('book requested')
  }
}
</script>

<style></style>
<v-select
  v-model="exchangeType"
  :items="items"
  label="الكتاب الذي تريده ... ؟"
  required
>
              </v-select>
<!-- Specefic Book -->
<div v-if="exchangeType == 'كتاب محدد'">
                <v-text-field
                  label="إسم الكتاب المطلوب"
                  required
                ></v-text-field>
                <v-text-field label="إسم الكاتب" required></v-text-field>
                <v-text-field label="سنة النشر"></v-text-field>
                <v-text-field
                  label="الرقم العالمي الموحد للكتاب (isbn)"
                ></v-text-field>
              </div>
<!-- Any Book From specefic Category -->
<div v-if="exchangeType == 'أي كتاب من تصنيف معين'">
                <v-select
                  v-model="wantedBookCategory"
                  :items="categories"
                  label="تصنيف الكتاب المطلوب"
                  required
                ></v-select>
              </div>
