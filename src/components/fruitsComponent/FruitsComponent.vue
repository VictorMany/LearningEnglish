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
        margin-bottom: -0.3rem;
        width: 100%;
        padding: 0.4rem;
        border-radius: 0.5rem;
        align: center;
        font-weight: bold;
      "
      class="bg-blue-13 text-white text-center"
    >
      Fruit
    </h4>
    <div class="row justify-around" style="margin-bottom: 1rem">
      <audio id="red"><source src="colors/red.mp3" /></audio>
      <audio id="blue"><source src="colors/blue.mp3" /></audio>
      <audio id="yellow"><source src="colors/yellow.mp3" /></audio>
      <audio id="green"><source src="colors/green.mp3" /></audio>
      <audio id="orange"><source src="colors/orange.mp3" /></audio>
      <audio id="purple"><source src="colors/purple.mp3" /></audio>
      <audio id="grey"><source src="colors/grey.mp3" /></audio>
      <audio id="pink"><source src="colors/pink.mp3" /></audio>
      <audio id="white"><source src="colors/white.mp3" /></audio>
      <audio id="correct"><source src="numbers/sounds/correct.mp3" /></audio>
      <audio id="incorrect">
        <source src="numbers/sounds/incorrect.mp3" />
      </audio>
    </div>

    <div class="row q-col-gutter-xs">
      <div class="col-6" v-for="n in arrayImagesColors" :key="n.id">
        <div style="padding: 0.3rem">
          <card-fruits
            :imagen="n.imagen"
            :color="n.color"
            :audio="n.id"
            :textoEspaniol="n.textoEspaniol"
            :textoIngles="n.textoIngles"
          ></card-fruits>
        </div>
      </div>
    </div>

    <q-btn
      push
      style="height: 40px; width: 100%; margin-top: 1rem"
      label="CLOSE"
      color="red-10"
      v-close-popup
      ><p style="font-size: 0.5rem; margin-left: 0.5rem">(Cerrar)</p></q-btn
    >
  </div>
</template>

<script>
import CardFruits from "./CardFruits.vue";
export default {
  components: { CardFruits },
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
      
      arrayImagesColors: [
        {
          id: 1,
          imagen: "img/fruits/aguacate.png",
          color: "red-13",
          textoEspaniol: "Aguacate",
          audio: "Red",
          textoIngles: "AVOCADO",
        },
        {
          id: 2,
          imagen: "img/fruits/arandano.png",
          color: "yellow-13",
          textoEspaniol: "Arándano",
          audio: "Yellow",
          textoIngles: "BLUEBERRY",
        },
        {
          id: 3,
          imagen: "img/fruits/frambuesa.png",
          color: "blue-7",
          textoEspaniol: "Frambuesa",
          audio: "Blue",
          textoIngles: "RASPBERRY",
        },
        {
          id: 4,
          imagen: "img/fruits/fresa.png",
          color: "green-13",
          textoEspaniol: "Fresa",
          audio: "Green",
          textoIngles: "STRAWBERRY",
        },
        {
          id: 5,
          imagen: "img/fruits/limon.png",
          color: "orange",
          textoEspaniol: "Limón",
          audio: "Orange",
          textoIngles: "LEMON",
        },
        {
          id: 6,
          imagen: "img/fruits/mandarina.png",
          color: "purple",
          textoEspaniol: "Mandarina",
          audio: "Purple",
          textoIngles: "TANGERINE",
        },
        {
          id: 7,
          imagen: "img/fruits/mango.png",
          color: "grey",
          textoEspaniol: "Mango",
          audio: "Grey",
          textoIngles: "MANGO",
        },
        {
          id: 8,
          imagen: "img/fruits/melon.png",
          color: "pink",
          textoEspaniol: "Melón",
          audio: "Pink",
          textoIngles: "MELON",
        },
        {
          id: 9,
          imagen: "img/fruits/papaya.png",
          color: "red-13",
          textoEspaniol: "Papaya",
          audio: "White",
          textoIngles: "PAPAYA",
        },
        {
          id: 10,
          imagen: "img/fruits/pepino.png",
          color: "yellow-13",
          textoEspaniol: "Pepino",
          audio: "White",
          textoIngles: "CUCUMBER",
        },
        {
          id: 11,
          imagen: "img/fruits/piña.png",
          color: "blue-7",
          textoEspaniol: "Piña",
          audio: "White",
          textoIngles: "PINEAPPLE",
        },
        {
          id: 12,
          imagen: "img/fruits/platano.png",
          color: "green-13",
          textoEspaniol: "Plátano",
          audio: "White",
          textoIngles: "BANANA",
        },
        {
          id: 13,
          imagen: "img/fruits/sandia.png",
          color: "orange",
          textoEspaniol: "Sandía",
          audio: "White",
          textoIngles: "WATERMELON",
        },
        {
          id: 14,
          imagen: "img/fruits/uva.png",
          color: "purple",
          textoEspaniol: "Uva",
          audio: "White",
          textoIngles: "GRAPE",
        },
        {
          id: 15,
          imagen: "img/apple.png",
          color: "grey",
          textoEspaniol: "Manzana",
          audio: "White",
          textoIngles: "APPLE",
        },
        {
          id: 16,
          imagen: "img/colors_orange.jpg",
          color: "pink",
          textoEspaniol: "Naranja",
          audio: "White",
          textoIngles: "ORANGE",
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

.qScrollStyle
  height: 100%
  width: 100%
</style>

