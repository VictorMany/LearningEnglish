<template>
  <div
    class="q-pa-md"
    style="width: 100%; height: 90%; background-color: rgb(10, 10, 10, 0.8)"
  >
    <h6
      style="
        margin-top: -0.3rem;
        margin-bottom: 1rem;
        width: 100%;
        padding: 0.4rem;
        border-radius: 0.5rem;
        text-align: center;
        font-weight: bold;
      "
      class="bg-blue-13 text-white"
    >
      Personal pronouns
    </h6>

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
      <q-btn
        style="width: 100%; height: auto"
        push
        class="q-btn"
        @click="cargarAudiosPronounsAleatorio"
        color="light-blue-13"
        icon="campaign"
      >
        <div class="row justify-center" style="width: 100%">CLICK ME !!</div>
        <p class="row justify-center text-white" style="font-size: 0.6rem">
          Presioname
        </p>
      </q-btn>
      <div
        class="col-5 bg-yellow-10 row justify-center content-center"
        style="height: 80px; border-radius: 0.5rem; margin: 0.5rem"
        @click="comprobar('i')"
      >
        <q-item-label class="text-white self-center text-bold text-h6"
          >Yo</q-item-label
        >
      </div>
      <div
        class="col-5 bg-yellow-10 row justify-center content-center"
        style="height: 80px; border-radius: 0.5rem; margin: 0.5rem"
        @click="comprobar('you')"
      >
        <q-item-label
          class="text-white self-center text-bold text-h6"
          style="overflow: scroll; padding: 0.56rem"
          >Tú/Ustedes</q-item-label
        >
      </div>
      <div
        class="col-5 bg-yellow-10 row justify-center content-center"
        style="height: 80px; border-radius: 0.5rem; margin: 0.5rem"
        @click="comprobar('they')"
      >
        <q-item-label class="text-white self-center text-bold text-h6"
          >Ellos</q-item-label
        >
      </div>
      <div
        class="col-5 bg-yellow-10 row justify-center content-center"
        style="height: 80px; border-radius: 0.5rem; margin: 0.5rem"
        @click="comprobar('we')"
      >
        <q-item-label class="text-white self-center text-bold text-h6"
          >Nosotros</q-item-label
        >
      </div>
      <div
        class="col-5 bg-yellow-10 row justify-center content-center"
        style="height: 80px; border-radius: 0.5rem; margin: 0.5rem"
        @click="comprobar('she')"
      >
        <q-item-label class="text-white self-center text-bold text-h6"
          >Ella</q-item-label
        >
      </div>
      <div
        class="col-5 bg-yellow-10 row justify-center content-center"
        style="height: 80px; border-radius: 0.5rem; margin: 0.5rem"
        @click="comprobar('he')"
      >
        <q-item-label class="text-white self-center text-bold text-h6"
          >Él</q-item-label
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
        @click="comprobar('it')"
      >
        <q-item-label class="text-white self-center text-bold text-h6"
          >Esto</q-item-label
        >
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

    <div style="margin-top: 2rem; margin-bottom: 1rem">
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
          class="bg-negative col text-center"
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
            Si obtienes un rojo es que deberías de estudiar más los pronombres
          </p>
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
export default {
  data() {
    return {
      numbers_0_20: false,
      numbers_tens: false,
      numbers_hundreds: false,
      numbers_thousands: false,
      text: "",
      ph: "",

      dense: false,

      arregloPronouns: [
        { number: 0, ruta: "i" },
        { number: 1, ruta: "you" },
        { number: 2, ruta: "they" },
        { number: 3, ruta: "we" },
        { number: 4, ruta: "he" },
        { number: 5, ruta: "she" },
        { number: 6, ruta: "it" },
      ],

      currentObject: {},
    };
  },

  methods: {
    async cargarAudio(sound) {
      console.log(sound.ruta, sound.number);
      var number = document.getElementById(sound.ruta);
      await number.play();
    },

    cargarAudiosPronounsAleatorio() {
      let number = Math.floor(Math.random() * (8 - 0) + 0);
      this.arregloPronouns.map((x) => {
        if (x.number == number) {
          this.cargarAudio(x);
          this.currentObject = { ...x };
        }
      });
    },

    async comprobar(text) {
      try {
        console.log("Numero del input", text);
        console.log("Numero dicho de voz", this.currentObject.number);

        if (text === this.currentObject.ruta.toString()) {
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
        this.cargarAudio(this.currentObject);
      } catch (error) {}
    },
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
