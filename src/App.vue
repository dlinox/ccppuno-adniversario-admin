<template>
  <v-app id="inspire">
    <v-app-bar class="px-3">
      <v-avatar
        color="grey-darken-1"
        class="hidden-md-and-up"
        size="32"
      ></v-avatar>

      <v-spacer></v-spacer>

      <v-tabs centered color="grey-darken-2" v-model="tab">
        <v-tab
          v-for="(link, index) in links"
          :key="link"
          :text="link"
          :value="link"
        ></v-tab>
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
        <v-window>
          <v-window-item >
            <WindowDashboar v-if="tab === 'Dashboard'" />
            <WindowPays v-if="tab === 'Pagos'" />
            <WindowControl v-if="tab === 'Control'" />
          </v-window-item>
        </v-window>
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup>
import { ref } from "vue";
import WindowPays from "@/components/WindowPays.vue";
import WindowControl from "@/components/WindowControl.vue";
import WindowDashboar from "@/components/WindowDashboar.vue";

const tab = ref("Dashboard");
const links = ["Dashboard", "Pagos", "Control"];
</script>
