<template>
  <v-app id="inspire">
    <v-app-bar class="px-3">
      <v-avatar
        color="grey-darken-1"
        class="hidden-md-and-up"
        size="32"
      ></v-avatar>

      <v-spacer></v-spacer>

      <v-tabs centered color="grey-darken-2">
        <v-tab v-for="link in links" :key="link" :text="link"></v-tab>
      </v-tabs>
      <v-spacer class="hidden-sm-and-down"></v-spacer>

      <v-avatar
        class="hidden-sm-and-down"
        color="grey-darken-1"
        size="32"
      ></v-avatar>
    </v-app-bar>

    <v-main class="bg-grey-lighten-3">
      <v-container>
        <v-window v-model="window" show-arrows>
          <v-window-item v-for="n in length" :key="n">
            <v-card height="200px" class="d-flex justify-center align-center">
              <span class="text-h2">Card {{ n }}</span>
            </v-card>
          </v-window-item>
        </v-window>
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup>
const links = ["Dashboard", "Pagos", "Control"];
</script>
