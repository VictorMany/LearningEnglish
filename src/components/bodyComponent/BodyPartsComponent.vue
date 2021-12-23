<template>
  <div
    class="q-pa-md"
    style="
      width: 100%;
      height: 90%;
      background-color: rgb(10, 10, 10, 0.8);
      overflow: scroll;
    "
  >
    <h4
      style="
        margin-top: -0.3rem;
        margin-bottom: 1rem;
        width: 100%;
        padding: 0.4rem;
        border-radius: 0.5rem;
        align: center;
        font-weight: bold;
      "
      class="bg-blue-13 text-white text-center"
    >
      Body parts
    </h4>

    <div class="row q-col-gutter-xs">
      <div class="col-6" v-for="n in arrayBodyPart" :key="n.id">
        <div style="padding: 0.3rem">
          <card-parts
            class="btn-card"
            :imagen="n.imagen"
            :color="n.color"
            :audio="n.id"
            :textoEspaniol="n.textoEspaniol"
            :textoIngles="n.textoIngles"
          ></card-parts>
        </div>
      </div>
    </div>

    <q-btn
      push
      style="height: 38px; width: 100%; margin-top: 1rem; padding-top: 0rem"
      label="CLOSE"
      color="red-10"
      v-close-popup
      ><p style="font-size: 0.5rem; margin-left: 0.5rem">(Cerrar)</p></q-btn
    >
  </div>
</template>

<script>
import CardParts from "./CardParts.vue";
export default {
  components: { CardParts },
  created() {
    this.imagen = "img/colors_grey.png";
    this.color = "grey-13";
    this.textoEspaniol = "";
    this.audio = 1;
    this.textoIngles = "";
  },
  data() {
    return {
      numbers_0_20: false,
      numbers_tens: false,
      numbers_hundreds: false,
      numbers_thousands: false,
      text: "",
      ph: "",

      /*Avocado, Blueberry, Raspberry,
      Strawberry, Lemon, Tangerine,
      Mango,
      Melon,
      Papaya,
      Cucumber,
      Pineapple,
      Banana,
      Watermelon,
      Grape,
      Apple,
      Orange
      */

      arrayBodyPart: [
        {
          id: 1,
          imagen: "img/bodyParts/brazo.jpeg",
          color: "red-13",
          textoEspaniol: "Brazo",
          audio: "arm",
          textoIngles: "ARM",
        },
        {
          id: 2,
          imagen: "img/bodyParts/cuello.png",
          color: "yellow-13",
          textoEspaniol: "Cuello",
          audio: "neck",
          textoIngles: "NECK",
        },
        {
          id: 3,
          imagen: "img/bodyParts/ear.png",
          color: "blue-7",
          textoEspaniol: "Oreja",
          audio: "ear",
          textoIngles: "EAR",
        },
        {
          id: 4,
          imagen: "img/bodyParts/feet.png",
          color: "green-13",
          textoEspaniol: "Pie",
          audio: "foot",
          textoIngles: "FOOT",
        },
        {
          id: 5,
          imagen: "img/bodyParts/finger.webp",
          color: "orange",
          textoEspaniol: "Dedo",
          audio: "finger",
          textoIngles: "FINGER",
        },
        {
          id: 6,
          imagen: "img/bodyParts/hand.png",
          color: "purple",
          textoEspaniol: "Mano",
          audio: "hand",
          textoIngles: "HAND",
        },
        {
          id: 7,
          imagen: "img/bodyParts/head.jpg",
          color: "grey",
          textoEspaniol: "Cabeza",
          audio: "head",
          textoIngles: "HEAD",
        },
        {
          id: 8,
          imagen: "img/bodyParts/legs.jpg",
          color: "pink",
          textoEspaniol: "Piernas",
          audio: "legs",
          textoIngles: "LEGS",
        },
        {
          id: 9,
          imagen: "img/bodyParts/nose.jpeg",
          color: "red-13",
          textoEspaniol: "Nariz",
          audio: "nose",
          textoIngles: "NOSE",
        },
        {
          id: 10,
          imagen: "img/bodyParts/ojos.jpeg",
          color: "yellow-13",
          textoEspaniol: "Ojos",
          audio: "eyes",
          textoIngles: "Eyes",
        },
      ],
      color: "",
      imagen: "",
      textoEspaniol: "",
      textoIngles: "",
      audio: "",
      dense: false,
    };
  },
};

//etiquetaAudio.play();
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

.btn-card:hover
  transform: scale(1.05)
  transition: .2s
  z-index: 1000

.qScrollStyle
  height: 100%
  width: 100%
</style>

