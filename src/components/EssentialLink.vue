<template>
  <div>
    <q-item
      :class="'bg-' + color"
      style="border-radius: 0.5rem; margin: 0.5rem; font-weight: bold"
      clickable
      tag="a"
      @click="openDialog(questionDialog)"
    >
      <q-item-section v-if="icon" avatar>
        <q-icon :name="icon" />
      </q-item-section>

      <q-item-section>
        <q-item-label style="font-weight: bold">{{ title }}</q-item-label>
        <q-item-label caption>
          {{ caption }}
        </q-item-label>
      </q-item-section>
    </q-item>

    <q-dialog
      v-model="numbers"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <numbers-component-questions></numbers-component-questions>
    </q-dialog>

    <q-dialog
      v-model="colors"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <colors-component-questions></colors-component-questions>
    </q-dialog>
  </div>
</template>

<script>
import { defineComponent } from "@vue/composition-api";
import NumbersComponentQuestions from "./NumbersComponentQuestions.vue";
import ColorsComponentQuestions from "./ColorsComponentQuestions.vue";

export default defineComponent({
  name: "EssentialLink",
  components: {
    NumbersComponentQuestions,
    ColorsComponentQuestions,
  },
  props: {
    title: {
      type: String,
      required: true,
    },

    caption: {
      type: String,
      default: "",
    },

    color: {
      type: String,
      default: "#",
    },

    icon: {
      type: String,
      default: "",
    },

    questionDialog: {
      type: String,
      default: "",
    },
  },

  data() {
    return {
      numbers: false,
      colors: false,
    };
  },
  methods: {
    openDialog(questionDialog) {
      console.log(questionDialog);
      switch (questionDialog) {
        case "numbers":
          this.numbers = true;
          break;
        case "colors":
          this.colors = true;
          break;
      }
    },
    crearAudio(sound) {
      var number = document.getElementById(sound);
      number.play();
    },
  },
});
</script>



<style lang="sass" scoped>
.button
  color: $blue
  padding: 0.3rem
  margin: 0.2rem

.q-btn
  width: 30%
  height: 70px
  margin-bottom: 0.5rem
  padding-top: 0.3rem

.q-btn_mitad
  width: 45%
  height: 70px
  margin-bottom: 0.5rem
  padding-top: 0.3rem

h6
  margin-top: -0.5rem

</style>