<template>
  <v-app id="inspire">
    <v-app-bar class="px-3 headerBar" color="white" flat density="compact">
      <v-spacer></v-spacer>

      <v-tabs centered color="white">
        <v-tab v-for="link in links" :key="link">
          {{ link }}
        </v-tab>
      </v-tabs>
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-main class="bg-grey-lighten-1">
      <v-container>
        <v-row>
          <v-col cols="12" sm="2"> </v-col>

          <v-col cols="12" sm="8">
            <v-sheet class="sheetStyle" min-height="70vh" rounded="lg">
              <v-row>
                <v-text-field variant="outlined"></v-text-field>
                <v-btn> Button </v-btn>
              </v-row>
            </v-sheet>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    links: ["Home", "About"],
  }),
};
</script>

<style scoped>
.sheetStyle {
  background-color: #ffffff;
}
.headerBar {
  background-color: #226089 !important;
}
</style>
