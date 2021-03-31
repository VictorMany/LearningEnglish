<template>
  <div class="bg-dark" style="width: 100%">
    <q-img
      :ratio="8 / 16"
      class="img-class"
      style="min-width: 313px"
      src="img/fondo.jpg"
      height="100%"
    >
      <q-scroll-area
        :thumb-style="thumbStyle"
        :bar-style="barStyle"
        class="qScrollStyle"
      >
        <div class="row" style="width: 100%; height; 100%;">
          <div class="col-6" style="padding: 1rem">
            <div
              class="div-menu bg-red-14"
              @click="numbers = true"
              style="overflow: hidden"
            >
              <div class="column items-center">
                <h6>Numbers</h6>
                <p>(Números)</p>
                <q-img
                  src="img/numbers.png"
                  style="width: 50%; height: 50%; margin-top: -0.6rem"
                />
              </div>
            </div>
            <div
              class="div-menu inset-shadow-down bg-cyan-14"
              @click="colors = true"
            >
              <div class="column items-center">
                <h6>Colors</h6>
                <p>(Colores)</p>
                <q-img
                  src="img/colors.png"
                  style="width: 80%; height: 80%; margin-top: -1.5rem"
                />
              </div>
            </div>

            <div
              class="div-menu inset-shadow-down bg-blue-14"
              @click="alphabet = true"
            >
              <div class="column items-center">
                <h6>Alphabet</h6>
                <p>(Abecedario)</p>
                <q-img
                  src="img/alphabet.png"
                  style="width: 80%; height: 80%; margin-top: -0.7rem"
                />
              </div>
            </div>

            <div
              class="div-menu inset-shadow-down bg-orange-14"
              @click="pronouns = true"
            >
              <div class="column items-center">
                <h6>Pronouns</h6>
                <p>(Pronombres personales)</p>
                <q-img src="img/pronouns.png" style="width: 60%; height: 60%" />
              </div>
            </div>
          </div>
          <div class="col-6" style="padding: 1rem">
            <div
              class="div-menu inset-shadow-down bg-purple-14"
              @click="fruits = true"
            >
              <div class="column items-center">
                <h6>Fruits</h6>
                <p>(Frutas)</p>
                <q-img src="img/apple.png" style="width: 50%; height: 50%" />
              </div>
            </div>

            <div
              class="div-menu inset-shadow-down bg-blue"
              @click="basic_phrases = true"
            >
              <div class="column items-center">
                <h6>Phrases</h6>
                <p>(Frases)</p>
                <q-img src="img/hi.png" style="width: 60%; height: 60%" />
              </div>
            </div>
            <div
              class="div-menu inset-shadow-down bg-green-14"
              @click="actions = true"
            >
              <div class="column items-center">
                <h6>Verbs</h6>
                <p>(Verbos)</p>
                <q-img
                  src="img/verbs.png"
                  style="width: 60%; height: 60%; margin-top: -0.6rem"
                />
              </div>
            </div>
            <div
              class="div-menu inset-shadow-down bg-amber-14"
              @click="body_parts = true"
            >
              <div class="column items-center">
                <h6>Body parts</h6>
                <p>(Partes del cuerpo)</p>
                <q-img
                  src="img/body.png"
                  style="width: 60%; height: 60%; margin-top: -1rem"
                />
              </div>
            </div>
          </div>
        </div>
      </q-scroll-area>
    </q-img>

    <q-dialog
      v-model="numbers"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <q-card
        style="width: 100%; background-color: rgb(10, 10, 10, 0.8); overflow: scroll"
      >
        <q-card-section
          class="bg-blue-10 text-white"
          style="border-radius: 0.5rem; margin: 1rem;"
        >
          <div class="text-h6">
            Numbers
          </div>

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

    <q-dialog
      v-model="alphabet"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <q-card
        style="width: 100%; background-color: rgb(10, 10, 10, 0.8); overflow: scroll"
      >
        <q-card-section class="q-pt-none">
          <alphabet-component/>
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
      v-model="colors"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <colors-component></colors-component>
    </q-dialog>

    <q-dialog
      v-model="body_parts"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <q-card style="width: 100%">
        <q-card-section
          class="bg-blue-10 text-white"
          style="border-radius: 0.5rem; margin: 1rem"
        >
          <div class="text-h6">Body Parts</div>
          <p style="font-size: 1rem; color: grey">(Partes del cuerpo)</p>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <body-parts-component />
        </q-card-section>

        <q-card-actions>
          <q-btn
            push
            style="width: 100%; height: 100%; margin-top: 4rem"
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
      v-model="fruits"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <q-card style="width: 100%">
        <q-card-section
          class="bg-blue-10 text-white"
          style="border-radius: 0.5rem; margin: 1rem"
        >
          <div class="text-h6">Fruits</div>
          <p style="font-size: 1rem; color: grey">(Frutas)</p>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <fruits-component />
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
      v-model="basic_phrases"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <q-card style="width: 100%">
        <q-card-section
          class="bg-blue-10 text-white"
          style="border-radius: 0.5rem; margin: 1rem"
        >
          <div class="text-h6">Basic Phrases</div>
          <p style="font-size: 1rem; color: grey">(Frases Básicas)</p>
        </q-card-section>
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

    <q-dialog
      v-model="actions"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <q-card style="width: 100%">
        <q-card-section
          class="bg-blue-10 text-white"
          style="border-radius: 0.5rem; margin: 1rem"
        >
          <div class="text-h6">Verbs</div>
          <p style="font-size: 1rem; color: grey">(Verbos)</p>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <actions-and-verbs-component />
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
      <q-card style="width: 100%">
        <q-card-section
          class="bg-blue-10 text-white"
          style="border-radius: 0.5rem; margin: 1rem"
        >
          <div class="text-h6">Verbs</div>
          <p style="font-size: 1rem; color: grey">(Verbos)</p>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <actions-and-verbs-component />
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
  </div>
</template>

<script lang="ts">
import { defineComponent } from "@vue/composition-api";
import ActionsAndVerbsComponent from "./actionsComponent/ActionsAndVerbsComponent.vue";
import AlphabetComponent from "./alphabetComponent/AlphabetComponent.vue";
import FruitsComponent from "./fruitsComponent/FruitsComponent.vue";
import BasicPhrasesComponent from "./phrasesComponent/BasicPhrasesComponent.vue";
import BodyPartsComponent from "./bodyComponent/BodyPartsComponent.vue";
import NumbersComponent from "./numbersComponent/NumbersComponent.vue";
import ColorsComponentQuestions from "./colorsComponent/ColorsComponentQuestions.vue";
import ColorsComponent from "./colorsComponent/ColorsComponent.vue";

export default defineComponent({
  components: {
    FruitsComponent,
    NumbersComponent,
    AlphabetComponent,
    BodyPartsComponent,
    BasicPhrasesComponent,
    ActionsAndVerbsComponent,
    ColorsComponentQuestions,
    ColorsComponent
  },
  name: "CompositionComponent",
  props: {
    title: {
      type: String,
      required: true
    },

    active: {
      type: Boolean
    }
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
        opacity: 0.75
      },
      barStyle: {
        right: "-6px",
        borderRadius: "9px",
        backgroundColor: "#027be3",
        width: "2px",
        opacity: 0.2
      }
    };
  },

  methods: {}
});
</script>

<style scoped lang="sass">
.div-menu
  width: 100%
  height: 150px
  color: white

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
