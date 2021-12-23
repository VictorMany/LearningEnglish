<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated style="height: 80px">
      <q-toolbar class="glossy bg-indigo-10">
        <q-btn
          style="width: 100px"
          flat
          dense
          round
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        >
          <q-icon size="80px" name="menu"> </q-icon
        ></q-btn>

        <q-toolbar-title class="text-white">
          <strong>LEARNING ENGLISH</strong>
          <p
            style="
              font-size: 0.8rem;
              margin-bottom: -0.1rem;
              
              font-weight: bold;
            "
            class="row text-grey"
          >
            (Aprendiendo inglés)
          </p>
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer
      class="bg-dark"
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-blue-1 text-white"
    >
      <q-list>
        <q-item-label header class="text-grey-8" style="font-weight: bold">
          QUESTIONS AREA
          <p
            style="
              margin-top: 0.5rem;
              margin-bottom: -1rem;
              font-size: 0.7rem;
              font-weight: normal;
            "
          >
            Área de preguntas
          </p>
        </q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">
import EssentialLink from "components/EssentialLink.vue";

const linksData = [
  {
    title: "Numbers",
    caption: "Numeros",
    icon: "pin",
    color: "red",
    questionDialog: "numbers",
  },
  {
    title: "Colors",
    caption: "colors",
    icon: "palette",
    color: "cyan",
    questionDialog: "colors",
  },
  {
    title: "Alphabet",
    caption: "Abecedario",
    icon: "sort_by_alpha",
    color: "blue-14",
    questionDialog: "alphabet",
  },
  {
    title: "Pronouns",
    caption: "Pronombres",
    icon: "groups",
    color: "orange-10",
    questionDialog: "pronouns",
  },
  {
    title: "Phrases",
    caption: "Frases",
    icon: "translate",
    color: "blue",
    questionDialog: "phrases",
  },
  {
    title: "Body parts",
    caption: "Partes del cuerpo",
    icon: "directions_run",
    color: "yellow-10",
    questionDialog: "body",
  },
  {
    title: "Verbs",
    caption: "Verbos",
    icon: "pedal_bike",
    color: "green-14",
    questionDialog: "actions",
  },

  {
    title: "Fruits",
    caption: "Frutas",
    icon: "icecream",
    color: "purple",
    questionDialog: "fruits",
  },
];

import { defineComponent, ref } from "@vue/composition-api";

export default defineComponent({
  name: "MainLayout",
  components: { EssentialLink },
  setup() {
    const leftDrawerOpen = ref(false);
    const essentialLinks = ref(linksData);

    return { leftDrawerOpen, essentialLinks };
  },
});
</script>
