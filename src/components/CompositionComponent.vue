<template>
  <div class="bg-indigo-3" style="width: 100%; height: 100%">
    <div class="row justify-evenly" style="width: 100%; height; 100%; margin-top: 1rem">
      <div
        class="div-menu col-4 col-md-4 col-lg-4 bg-white"
        @click="numbers = true"
        style="overflow: hidden"
      >
        <div class="column items-center text-red-14">
          <h6>Numbers</h6>
          <p>(Números)</p>
          <q-img
            basic
            src="img/numbers.gif"
            style="width: 70%; height: 70%; margin-top: -1rem"
          />
        </div>
      </div>
      <div
        class="div-menu col-6 col-md-4 col-lg-4 inset-shadow bg-white"
        @click="colors = true"
      >
        <div class="column items-center text-cyan-14">
          <h6>Colors</h6>
          <p>(Colores)</p>
          <q-img
            basic
            src="img/colors.gif"
            style="width: 65%; height: 60%; margin-top: -1rem"
          />
        </div>
      </div>
      <div
        class="div-menu col-6 col-md-4 col-lg-4 inset-shadow bg-white"
        @click="alphabet = true"
      >
        <div class="column items-center text-cyan-14">
          <h6>Alphabet</h6>
          <p>(Abecedario)</p>
          <q-img
            basic
            src="img/abc.gif"
            style="width: 70%; height: 70%; margin-top: -1rem"
          />
        </div>
      </div>
      <div
        class="
          div-menu
          col-6 col-md-4 col-lg-4
          inset-shadow
          bg-white
          text-orange-14
        "
        @click="pronouns = true"
      >
        <div class="column items-center">
          <h6>Pronouns</h6>
          <p>(Pronombres)</p>
          <q-img
            basic
            src="img/pronouns.gif"
            style="width: 70%; height: 70%; margin-top: -1rem"
          />
        </div>
      </div>

      <div
        class="div-menu col-6 col-md-4 col-lg-4 inset-shadow bg-white text-blue"
        @click="basic_phrases = true"
      >
        <div class="column items-center">
          <h6>Phrases</h6>
          <p>(Frases)</p>
          <q-img
            basic
            src="img/phrases.gif"
            style="width: 70%; height: 70%; margin-top: -1rem"
          />
        </div>
      </div>
      <div
        class="div-menu col-6 col-md-4 col-lg-4 inset-shadow bg-white text-blue"
        @click="fruits = true"
      >
        <div class="column items-center">
          <h6>Fruits</h6>
          <p>(Frutas)</p>
          <q-img
            basic
            src="img/apple.gif"
            style="width: 70%; height: 70%; margin-top: -1rem"
          />
        </div>
      </div>
      <div
        class="
          div-menu
          col-6 col-md-4 col-lg-4
          inset-shadow
          bg-white
          text-green-14
        "
        @click="actions = true"
      >
        <div class="column items-center">
          <h6>Verbs</h6>
          <p>(Verbos)</p>
          <q-img
            basic
            src="img/verbs.gif"
            style="width: 70%; height: 70%; margin-top: -1rem"
          />
        </div>
      </div>
      <div
        class="
          div-menu
          col-6 col-md-4 col-lg-4
          inset-shadow
          bg-white
          text-amber-14
        "
        @click="body_parts = true"
      >
        <div class="column items-center">
          <h6>Body parts</h6>
          <p>(Partes del cuerpo)</p>
          <q-img
            basic
            src="img/body.gif"
            style="width: 70%; height: 70%; margin-top: -1rem"
          />
        </div>
      </div>
    </div>

    <!--Numeros-->
    <q-dialog
      v-model="numbers"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <q-card
        style="
          width: 100%;
          background-color: rgb(10, 10, 10, 0.8);
          overflow: scroll;
        "
      >
        <q-card-section
          class="bg-blue-10 text-white"
          style="border-radius: 0.5rem; margin: 1rem"
        >
          <div class="text-h6">Numbers</div>

          <p style="font-size: 1rem; color: grey">(Números)</p>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <numbers-component />
        </q-card-section>

        <q-card-actions>
          <q-btn
            push
            style="width: 100%; height: 100%; width: 100%"
            label="CLOSE"
            color="red-10"
            v-close-popup
            ><p style="font-size: 0.5rem; margin-left: 0.5rem">
              (Cerrar)
            </p></q-btn
          >
        </q-card-actions>
      </q-card>
    </q-dialog>
    <!--Abecedario-->
    <q-dialog
      v-model="alphabet"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <q-card
        style="
          width: 100%;
          background-color: rgb(10, 10, 10, 0.8);
          overflow: scroll;
        "
      >
        <q-card-section class="q-pt-none">
          <alphabet-component />
        </q-card-section>

        <q-card-actions>
          <q-btn
            push
            style="width: 100%; height: 100%; width: 100%; margin-top: 4rem"
            label="CLOSE"
            color="red-10"
            v-close-popup
            ><p style="font-size: 0.5rem; margin-left: 0.5rem">
              (Cerrar)
            </p></q-btn
          >
        </q-card-actions>
      </q-card>
    </q-dialog>
    <!--Colores-->
    <q-dialog
      v-model="colors"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <colors-component></colors-component>
    </q-dialog>
    <!--Partes del cuerpo-->
    <q-dialog
      v-model="body_parts"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <body-parts-component />
    </q-dialog>
    <!--Frutas-->
    <q-dialog
      v-model="fruits"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <fruits-component />
    </q-dialog>
    <!--Frases básicas-->
    <q-dialog
      v-model="basic_phrases"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <q-card
        style="
          width: 100%;
          background-color: rgb(10, 10, 10, 0.8);
          overflow: scroll;
        "
      >
        <q-card-section class="q-pt-none">
          <basic-phrases-component />
        </q-card-section>

        <q-card-actions>
          <q-btn
            push
            style="width: 100%; height: 100%; width: 100%; margin-top: 4rem"
            label="CLOSE"
            color="red-10"
            v-close-popup
            ><p style="font-size: 0.5rem; margin-left: 0.5rem">
              (Cerrar)
            </p></q-btn
          >
        </q-card-actions>
      </q-card>
    </q-dialog>
    <!--Acciones y verbos-->
    <q-dialog
      v-model="actions"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <q-card
        style="
          width: 100%;
          background-color: rgb(10, 10, 10, 0.8);
          overflow: scroll;
        "
      >
        <q-card-section class="q-pt-none">
          <basic-verbs-component />
        </q-card-section>

        <q-card-actions>
          <q-btn
            push
            style="width: 100%; height: 100%; width: 100%; margin-top: 4rem"
            label="CLOSE"
            color="red-10"
            v-close-popup
            ><p style="font-size: 0.5rem; margin-left: 0.5rem">
              (Cerrar)
            </p></q-btn
          >
        </q-card-actions>
      </q-card>
    </q-dialog>

    <q-dialog
      v-model="pronouns"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <pronouns-component />
    </q-dialog>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "@vue/composition-api";
import AlphabetComponent from "./alphabetComponent/AlphabetComponent.vue";
import FruitsComponent from "./fruitsComponent/FruitsComponent.vue";
import BasicPhrasesComponent from "./phrasesComponent/BasicPhrasesComponent.vue";
import BodyPartsComponent from "./bodyComponent/BodyPartsComponent.vue";
import NumbersComponent from "./numbersComponent/NumbersComponent.vue";
import ColorsComponentQuestions from "./colorsComponent/ColorsComponentQuestions.vue";
import ColorsComponent from "./colorsComponent/ColorsComponent.vue";
import PronounsComponent from "./pronounsComponent/PronounsComponent.vue";
import BasicVerbsComponent from "./verbsComponent/BasicVerbsComponent.vue";

export default defineComponent({
  components: {
    FruitsComponent,
    NumbersComponent,
    AlphabetComponent,
    BodyPartsComponent,
    BasicPhrasesComponent,
    ColorsComponentQuestions,
    ColorsComponent,
    PronounsComponent,
    BasicVerbsComponent,
  },
  name: "CompositionComponent",
  props: {
    title: {
      type: String,
      required: true,
    },

    active: {
      type: Boolean,
    },
  },
  data() {
    return {
      actions: false,
      alphabet: false,
      body_parts: false,
      numbers: false,
      fruits: false,
      basic_phrases: false,
      pronouns: false,
      colors: false,
      thumbStyle: {
        right: "-6px",
        borderRadius: "1px",
        backgroundColor: "#027be3",
        width: "2px",
        opacity: 0.75,
      },
      barStyle: {
        right: "-6px",
        borderRadius: "9px",
        backgroundColor: "#027be3",
        width: "2px",
        opacity: 0.2,
      },
    };
  },

  methods: {},
});
</script>

<style scoped lang="sass">
.div-menu
  width: 45%
  padding: 1rem
  margin-bottom: 1rem
  border-radius: 1rem

p
  margin-top: -3rem
  color: light-grey
  font-weight: bold

h6
  margin-top: -0.2rem

.qScrollStyle
  height: calc(100%)
  width: 100%

.img-class
  height: 200%
  object-fit: cover

div
  overflow: hidden
</style>
