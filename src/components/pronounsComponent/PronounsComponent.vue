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
    <h5
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
      Personal pronouns
    </h5>

    <!--  DIV DE LOS AUDIOS-->
    <div>
      <audio id="i"><source src="pronouns/i.mp3" /></audio>
      <audio id="you"><source src="pronouns/you.mp3" /></audio>
      <audio id="they"><source src="pronouns/they.mp3" /></audio>
      <audio id="we"><source src="pronouns/we.mp3" /></audio>
      <audio id="she"><source src="pronouns/she.mp3" /></audio>
      <audio id="he"><source src="pronouns/he.mp3" /></audio>
      <audio id="it"><source src="pronouns/it.mp3" /></audio>

      <audio id="correct"><source src="numbers/sounds/correct.mp3" /></audio>
      <audio id="incorrect">
        <source src="numbers/sounds/incorrect.mp3" />
      </audio>
    </div>
    <!--  DIV DE LOS AUDIOS-->

    <div class="row justify-center content-center" style="width: 100%">
      <div
        class="col-5 bg-blue-13 row justify-center content-center"
        style="height: 80px; border-radius: 0.5rem; margin: 0.5rem"
        @click="crearAudio('i')"
      >
        <q-item-label class="text-white self-center text-bold text-h5"
          >I</q-item-label
        >
      </div>
      <div
        class="col-5 bg-red-13 row justify-center content-center"
        style="height: 80px; border-radius: 0.5rem; margin: 0.5rem"
        @click="crearAudio('you')"
      >
        <q-item-label class="text-white self-center text-bold text-h5"
          >You</q-item-label
        >
      </div>
      <div
        class="col-5 bg-green-13 row justify-center content-center"
        style="height: 80px; border-radius: 0.5rem; margin: 0.5rem"
        @click="crearAudio('they')"
      >
        <q-item-label class="text-white self-center text-bold text-h5"
          >They</q-item-label
        >
      </div>
      <div
        class="col-5 bg-purple-13 row justify-center content-center"
        style="height: 80px; border-radius: 0.5rem; margin: 0.5rem"
        @click="crearAudio('we')"
      >
        <q-item-label class="text-white self-center text-bold text-h5"
          >We</q-item-label
        >
      </div>
      <div
        class="col-5 bg-cyan-13 row justify-center content-center"
        style="height: 80px; border-radius: 0.5rem; margin: 0.5rem"
        @click="crearAudio('she')"
      >
        <q-item-label class="text-white self-center text-bold text-h5"
          >She</q-item-label
        >
      </div>
      <div
        class="col-5 bg-pink-13 row justify-center content-center"
        style="height: 80px; border-radius: 0.5rem; margin: 0.5rem"
        @click="crearAudio('he')"
      >
        <q-item-label class="text-white self-center text-bold text-h5"
          >He</q-item-label
        >
      </div>
      <div
        class="bg-yellow-10 row justify-center content-center"
        style="
          height: 80px;
          width: 100%;
          border-radius: 0.5rem;
          margin-right: 1.1rem;
          margin-left: 1.1rem;
          margin-top: 0.5rem;
        "
        @click="crearAudio('it')"
      >
        <q-item-label class="text-white self-center text-bold text-h5"
          >It</q-item-label
        >
      </div>
    </div>

    <div
      style="margin-top: 2rem; margin-bottom: 1rem"
      class="row justify-center"
    >
      <card-img-pronoun
        :imagen="imagen"
        :color="color"
        :audio="audio"
        :textoEspaniol="textoEspaniol"
        :textoIngles="textoIngles"
      ></card-img-pronoun>
    </div>
    <div
      style="margin-top: 2rem; margin-bottom: 1rem"
      class="row justify-center"
    >
      <card-img-pronoun
        v-if="you"
        :imagen="'img_pronouns/you_.png'"
        :color="color"
        :audio="audio"
        :textoEspaniol="'Tú'"
        :textoIngles="textoIngles"
      ></card-img-pronoun>
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
import CardImgPronoun from "./CardImgPronoun.vue";
export default {
  components: { CardImgPronoun },
  created() {
    this.imagen = "img_pronouns/i.png";
    this.color = "grey-13";
    this.textoEspaniol = "Yo";
    this.audio = "I";
    this.textoIngles = "I";
  },
  data() {
    return {
      numbers_0_20: false,
      numbers_tens: false,
      numbers_hundreds: false,
      numbers_thousands: false,
      text: "",
      ph: "",
      you: false,

      arrayImagesPronouns: [
        {
          id: 1,
          imagen: "img_pronouns/i.png",
          color: "red-13",
          textoEspaniol: "Yo",
          audio: "I",
          textoIngles: "I",
        },
        {
          id: 2,
          imagen: "img_pronouns/you.png",
          color: "yellow-13",
          textoEspaniol: "Ustedes",
          audio: "You",
          textoIngles: "You",
        },
        {
          id: 3,
          imagen: "img_pronouns/they.png",
          color: "blue-13",
          textoEspaniol: "Ellos",
          audio: "They",
          textoIngles: "They",
        },
        {
          id: 4,
          imagen: "img_pronouns/we.png",
          color: "green-13",
          textoEspaniol: "Nosotros",
          audio: "We",
          textoIngles: "We",
        },
        {
          id: 5,
          imagen: "img_pronouns/he.png",
          color: "orange",
          textoEspaniol: "Él",
          audio: "He",
          textoIngles: "He",
        },
        {
          id: 6,
          imagen: "img_pronouns/she.png",
          color: "purple",
          textoEspaniol: "Ella",
          audio: "She",
          textoIngles: "She",
        },
        {
          id: 7,
          imagen: "img_pronouns/it.png",
          color: "grey",
          textoEspaniol: "Esto/Esta",
          audio: "It",
          textoIngles: "It",
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
      this.arrayImagesPronouns.map((item) => {
        if (item.audio.toLowerCase() === sound.toLowerCase()) {
          console.log(item);
          this.color = item.color;
          this.imagen = item.imagen;
          this.textoIngles = item.textoIngles;
          this.textoEspaniol = item.textoEspaniol;
          this.audio = item.audio;
          this.you = false;
          if (sound === "you") {
            this.you = true;
          }
        }
      });
    },
  },
};

//etiquetaAudio.play();
</script>

<style lang="sass" scoped>
h6
  margin-top: -0.5rem

.qScrollStyle
  height: 100%
  width: 100%
</style>
