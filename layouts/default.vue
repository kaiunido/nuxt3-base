<template>
  <v-app>
    <v-navigation-drawer :rail="drawer" :expand-on-hover="drawer">
      <v-list density="compact" nav>
        <v-list-item
          prepend-icon="mdi-folder"
          title="Home"
          to="/"
        ></v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar order="-1">
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title class="text-uppercase">Tec Company</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <slot />
    </v-main>
  </v-app>
</template>

<script lang="ts" setup>
import { ref } from 'vue';

const drawer = ref(false);
</script>
