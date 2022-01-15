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
    <div>
      <audio id="correct"><source src="numbers/sounds/correct.mp3" /></audio>
      <audio id="incorrect">
        <source src="numbers/sounds/incorrect.mp3" />
      </audio>
    </div>
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
      BodyPart Questions
    </h4>

    <q-btn
      style="width: 100%; height: auto; margin-top: 1rem"
      push
      class="q-btn"
      @click="cargarAudiosColorsAleatorio"
      color="light-blue-13"
      icon="campaign"
    >
      <div class="row justify-center" style="width: 100%">CLICK ME !!</div>
      <p class="row justify-center text-white" style="font-size: 0.6rem">
        Presióname
      </p>
    </q-btn>

    <div class="row q-col-gutter-xs">
      <div class="col-6" v-for="n in arrayBodyPart" :key="n.id">
        <div style="padding: 0.3rem" @click="comprobar(n.id)">
          <card-parts
            class="body-card"
            :imagen="n.imagen"
            :color="n.color"
            :audio="n.id"
          ></card-parts>
        </div>
      </div>
    </div>

    <div class="row" style="margin-top: 1rem">
      <q-btn
        style="width: 100%; border-radius: 0.5rem"
        icon="repeat"
        class="bg-blue text-white"
        label="Repeat"
        @click="repeat"
      >
      </q-btn>
    </div>

    <div style="margin-top: 2.5rem; margin-bottom: 1rem">
      <div class="row justify-around text-white">
        <div
          class="bg-green-14 col text-center"
          style="
            padding: 0.5rem;
            border-radius: 0.5rem;
            font-weight: bold;
            margin: 0 0.5rem 0 0.5rem;
          "
        >
          <p
            style="
              background-color: rgb(0, 0, 0, 0.3);
              padding: 0.5rem;
              border-radius: 0.5rem;
            "
          >
            Good
          </p>
          <p
            class="text-grey-4 text-justify"
            style="
              background-color: rgb(0, 0, 0, 0.3);
              padding: 0.5rem;
              border-radius: 0.5rem;
            "
          >
            Si obtienes un verde es que vas muy bien :)
          </p>
        </div>
        <div
          class="bg-red-13 col text-center"
          style="
            padding: 0.5rem;
            border-radius: 0.5rem;
            font-weight: bold;
            margin: 0 0.5rem 0 0.5rem;
          "
        >
          <p
            style="
              background-color: rgb(0, 0, 0, 0.3);
              padding: 0.5rem;
              border-radius: 0.5rem;
            "
          >
            Wrong
          </p>
          <p
            class="text-grey-4 text-justify"
            style="
              background-color: rgb(0, 0, 0, 0.3);
              padding: 0.5rem;
              border-radius: 0.5rem;
            "
          >
            Si obtienes un rojo es que deberías de estudiar más las partes del
            cuerpo
          </p>
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
    this.audio = 0;
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

  methods: {
    crearAudio(sound) {
      var number = document.getElementById(sound);
      number.play();
      console.log(sound);
      this.arrayBodyPart.map((item) => {
        if (item.audio === sound) {
          console.log(item);
          this.color = item.color;
          this.imagen = item.imagen;
          this.textoIngles = item.textoIngles;
          this.textoEspaniol = item.textoEspaniol;
          this.audio = item.audio;
        }
      });
    },

    cargarAudiosColorsAleatorio() {
      let number = Math.floor(Math.random() * (11 - 0) + 0);
      this.arrayBodyPart.map((x) => {
        if (x.id == number) {
          this.crearAudio(x.id);
          this.currentObject = { ...x };
        }
      });
    },

    async comprobar(text) {
      try {
        if (text === this.currentObject.id) {
          var number = document.getElementById("correct");
          await number.play();
          this.$q.notify({
            type: "positive",
            message: `Vas muy bien !!`,
          });

          text = "";
        } else {
          var number = document.getElementById("incorrect");
          await number.play();

          this.$q.notify({
            type: "negative",
            message: `Try Again!!`,
          });
        }
      } catch (error) {}
    },

    repeat() {
      try {
        this.crearAudio(this.currentObject.id);
      } catch (error) {}
    },
  },
};

//etiquetaAudio.play();
</script>

<style lang="sass" scoped>
.q-btn
  width: 30%
  height: 70px
  margin-bottom: 0.5rem
  padding-top: 0.3rem


.body-card:hover
  transform: scale(1.05)
  transition: .2s
  z-index: 1000

h6
  margin-top: -0.5rem

.qScrollStyle
  height: 100%
  width: 100%
</style>

