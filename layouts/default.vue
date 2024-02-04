<template>
  <v-app>
    <v-app-bar color="transparent" :elevation="0">
      <template v-slot:prepend>
        <nuxt-link to="/">
          <v-icon icon="mdi-accountCancelOutline " size="large"></v-icon>
        </nuxt-link>
      </template>

      <v-app-bar-title>E-Invoice</v-app-bar-title>

      <template v-slot:append>
        <v-btn text="true">CamInv</v-btn>
        <v-btn text>Guideline</v-btn>
        <v-btn text>Features</v-btn>
        <v-btn text>Design Principles</v-btn>
        <v-btn text>Overview</v-btn>
        <v-btn text>Media</v-btn>
        <v-btn text>FAQ</v-btn>
        <v-btn @click="toggleTheme">Verification Tool</v-btn>
      </template>
    </v-app-bar>

    <slot />
  </v-app>
</template>

<script lang="ts" setup>
import { useTheme } from "vuetify";

const theme = useTheme();

const toggleTheme = () => {
  theme.global.name.value = theme.global.current.value.dark
    ? "lightTheme"
    : "darkTheme";
};
</script>

<style></style>
