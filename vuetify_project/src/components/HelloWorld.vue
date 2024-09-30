<template>
  <v-toolbar>
    <v-app-bar-nav-icon></v-app-bar-nav-icon>

    <v-toolbar-title>Vuetify </v-toolbar-title>

    <v-spacer></v-spacer>

    <v-btn
      color="pink"
      size="default"
      variant="outlined"
      text="Vuetify"
      rounded="xs"
    ></v-btn>
    <v-btn
      :loading="loading"
      size="default"
      variant="outlined"
      text="Vuetify"
      rounded="xs"
      :ripple="false"
    ></v-btn>
  </v-toolbar>

  <v-card class="pa-8 mx-auto" width="300">
    <v-card-iem>
      <v-card-title class="text-center">login here</v-card-title>
      <v-form @submit.prevent="submit">
        <v-text-field
          label="email"
          v-model="form.email"
          prepend-inner-icon="mdi-email"
          type="email"
        ></v-text-field>
        <v-text-field
          label="password"
          v-model="form.passWord"
          prepend-inner-icon="mdi-key"
          type="password"
        ></v-text-field>
        <v-checkbox
          v-model="form.remember"
          label="remember me"
          color="red"
        ></v-checkbox>
        <v-btn class="my-2" type="submit" block color="red-darken-1"
          >Submit</v-btn
        >
      </v-form>
    </v-card-iem>
    <v-card-action>
      <v-btn block>resgitter</v-btn>
    </v-card-action>
  </v-card>
  <v-card
    append-icon="mdi-check"
    class="mx-auto"
    prepend-icon="mdi-account"
    subtitle="prepend-icon and append-icon"
    title="Icons"
  >
    <v-card-text
      >Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
      eiusmod.</v-card-text
    >
  </v-card>
</template>

<script setup>
import { ref } from "vue";

const form = ref({
  email: "",
  passWord: "",
  remember: false,
});

const submit = () => {
  console.log(form.value);
};
</script>
