<template>
  <v-layout>
    <v-row>
      <!-- exchanges -->
      <v-col cols="9">
        <v-card flat>
          <v-card-title>الكتب المتوفرة / يمكنك الحصول على 4 كتب</v-card-title>
          <v-row>
            <v-col cols="4">
              <v-card class="pt-4">
                <div class="cover">رواية</div>
                <div class="mt-4 mr-4 ">إسم الكتاب : كتاب 1</div>
                <div class="mr-4">إسم الكاتب : الكتاب 111</div>
                <v-card-actions class="mx-2">
                  <v-btn class="primary" block>أطلب الكتاب</v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col cols="4">
              <v-card class="pt-4">
                <div class="cover">سيرة ذاتية</div>
                <div class="mt-4 mr-4">إسم الكتاب : كتاب 1</div>
                <div class="mr-4">إسم الكاتب : الكتاب 111</div>
                <v-card-actions class="mx-2">
                  <v-btn class="primary" block>أطلب الكتاب</v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col cols="4">
              <v-card class="pt-4">
                <div class="cover">أعمال</div>
                <div class="mt-4 mr-4">إسم الكتاب : كتاب 1</div>
                <div class="mr-4">إسم الكاتب : الكتاب 111</div>
                <v-card-actions class="mx-2">
                  <v-btn class="primary" block>أطلب الكتاب</v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
          </v-row>
        </v-card>
      </v-col>

      <!-- Categories -->
      <v-col cols="3">
        <v-btn
          large
          block
          color="deep-purple"
          to="/exchange/create"
          class="primary my-4"
          >أطلب كتاب</v-btn
        >
        <v-card outlined>
          <v-card-title>التصنيفات</v-card-title>
          <v-list>
            <v-list-item v-for="category in categories" :key="category">
              <v-list-item-content>
                <v-list-item-title v-text="category"></v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
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
      categories: ['روايات', 'أعمال', 'سيرة ذاتية', 'رياضيات', 'أطفال']
    }
  }
}
</script>

<style scoped>
.cover {
  display: block;
  background-color: #ccc;
  width: 60%;
  height: 200px;
  margin: 0 auto;
  text-align: center;
}
</style>

<v-col cols="9">
        <v-card flat>
          <v-card-title>الكتب المتوفرة</v-card-title>
          <v-container fluid>
            <!-- first row -->
            <v-card>
              <v-row>
                <v-col>
                  <v-card-title> الكتاب المقدم</v-card-title>
                  <v-card-text>
                    <div>إسم الكتاب : learn php</div>
                    <div>الكاتب : robin nixon</div>
                  </v-card-text>
                </v-col>
                <v-divider class=" my-4" vertical></v-divider>
                <v-col>
                  <v-card-title> الكتاب المطلوب</v-card-title>
                  <v-card-text>
                    <div>إسم الكتاب : learn node</div>
                    <div>الكاتب : John Doe</div>
                  </v-card-text>
                </v-col>
              </v-row>
              <v-card-actions>
                <v-btn large color="deep-purple" class="white--text"
                  >تلبية الطلب</v-btn
                >
              </v-card-actions>
            </v-card>
            <!-- second row  -->
            <v-card class="mt-4">
              <v-row>
                <v-col>
                  <v-card-title> الكتاب المقدم</v-card-title>
                  <v-card-text>
                    <div>إسم الكتاب : learn php</div>
                    <div>الكاتب : robin nixon</div>
                  </v-card-text>
                </v-col>
                <v-divider class=" my-4" vertical></v-divider>

                <v-col>
                  <v-card-title> الكتاب المطلوب</v-card-title>
                  <v-card-text>
                    مطلوب أي كتاب في تصنيف روايات عالمية
                  </v-card-text>
                </v-col>
              </v-row>
              <v-card-actions>
                <v-btn large color="deep-purple" class="white--text"
                  >تلبية الطلب</v-btn
                >
              </v-card-actions>
            </v-card>
          </v-container>
        </v-card>
      </v-col>
