<template>
  <v-app>
    <v-toolbar
      image="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
      dark
      prominent
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Vuetify</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-export</v-icon>
      </v-btn>
    </v-toolbar>
    <v-content class="pt-5">
      <v-row dense>
        <v-col v-for="(variant, i) in variants" :key="i" cols="12" md="4">
          <v-card
            :variant="variant"
            class="mx-auto"
            color="surface-variant"
            max-width="344"
            subtitle="Greyhound divisely hello coldly fonwderfully"
            title="Headline"
          >
            <template v-slot:actions>
              <v-btn text="Button"></v-btn>
            </template>
          </v-card>

          <div class="text-center text-caption">{{ variant }}</div>
        </v-col>
      </v-row>
    </v-content>
    <v-footer border>Copy right Rath</v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    variants: ["elevated", "flat", "tonal", "outlined", "text", "plain"],
  }),
};
</script>
