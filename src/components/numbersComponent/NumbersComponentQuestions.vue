<template>
  <div
    class="q-pa-md"
    style="width: 100%; height: 90%; background-color: rgb(10, 10, 10, 0.8)"
  >
    <h4
      style="
        margin-top: -0.3rem;
        margin-bottom: 2rem;
        width: 100%;
        padding: 0.4rem;
        border-radius: 0.5rem;
        text-align: center;
        font-weight: bold;
      "
      class="bg-blue-13 text-white"
    >
      Numbers
    </h4>
    <div class="row justify-around" style="margin-bottom: 2rem">
      <audio id="zero"><source src="numbers/zero.mp3" /></audio>
      <audio id="one"><source src="numbers/one.mp3" /></audio>
      <audio id="two"><source src="numbers/two.mp3" /></audio>
      <audio id="three"><source src="numbers/three.mp3" /></audio>
      <audio id="four"><source src="numbers/four.mp3" /></audio>
      <audio id="five"><source src="numbers/five.mp3" /></audio>
      <audio id="six"><source src="numbers/six.mp3" /></audio>
      <audio id="seven"><source src="numbers/seven.mp3" /></audio>
      <audio id="eight"><source src="numbers/eight.mp3" /></audio>
      <audio id="nine"><source src="numbers/nine.mp3" /></audio>
      <audio id="ten"><source src="numbers/ten.mp3" /></audio>
      <audio id="eleven"><source src="numbers/eleven.mp3" /></audio>
      <audio id="twelve"><source src="numbers/twelve.mp3" /></audio>
      <audio id="thirteen"><source src="numbers/thirteen.mp3" /></audio>
      <audio id="fourteen"><source src="numbers/fourteen.mp3" /></audio>
      <audio id="fifteen"><source src="numbers/fifteen.mp3" /></audio>
      <audio id="sixteen"><source src="numbers/sixteen.mp3" /></audio>
      <audio id="seventeen"><source src="numbers/seventeen.mp3" /></audio>
      <audio id="eighteen"><source src="numbers/eighteen.mp3" /></audio>
      <audio id="nineteen"><source src="numbers/nineteen.mp3" /></audio>
      <audio id="twenty"><source src="numbers/twenty.mp3" /></audio>
      <audio id="correct"><source src="numbers/sounds/correct.mp3" /></audio>
      <audio id="incorrect">
        <source src="numbers/sounds/incorrect.mp3" />
      </audio>

      <q-btn
        style="width: 100%; height: auto"
        push
        class="q-btn"
        @click="cargarAudiosAleatorio"
        color="light-blue-13"
        icon="campaign"
      >
        <div class="row justify-center" style="width: 100%">CLICK ME !!</div>
        <p class="row justify-center text-white" style="font-size: 0.6rem">
          Presioname
        </p>
      </q-btn>
    </div>

    <q-input
      class="bg-blue-3 text-white"
      bottom-slots
      type="number"
      v-model="text"
      label="Escribe el número que escuches"
      :dense="dense"
      style="padding: 0.5rem; height: auto; border-radius: 1rem; color: white"
    >
      <template v-slot:append>
        <q-icon
          v-if="text !== ''"
          name="close"
          @click="text = ''"
          class="cursor-pointer text-white"
        />
      </template>

      <template v-slot:after>
        <q-btn
          style="width: 100%; height: 40px; padding: 0.2rem"
          round
          dense
          color="green-10 bg-green-13"
          push
          icon="send"
          @click="comprobar"
        />
        <q-btn
          style="width: 100%; height: 40px; padding: 0.2rem"
          round
          dense
          color="blue-10 bg-blue"
          push
          icon="repeat"
          @click="repeat"
        />
      </template>
    </q-input>

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
            style="background-color: rgb(0,0,0, 0.3); padding: 0.5rem; border-radius: 0.5rem"
          >
            Good
          </p>

          <p
            class="text-grey-4 text-justify"
            style="background-color: rgb(0,0,0, 0.3); padding: 0.5rem; border-radius: 0.5rem"
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
            style="background-color: rgb(0,0,0, 0.3); padding: 0.5rem; border-radius: 0.5rem"
          >
            Wrong
          </p>
          <p
            class="text-grey-4 text-justify"
            style="background-color: rgb(0,0,0, 0.3); padding: 0.5rem; border-radius: 0.5rem"
          >
            Si obtienes un rojo es que deberías de estudiar más los números
          </p>
        </div>
      </div>
    </div>
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
      arregloAudios: [
        { number: 0, ruta: "zero" },
        { number: 1, ruta: "one" },
        { number: 2, ruta: "two" },
        { number: 3, ruta: "three" },
        { number: 4, ruta: "four" },
        { number: 5, ruta: "five" },
        { number: 6, ruta: "six" },
        { number: 7, ruta: "seven" },
        { number: 8, ruta: "eight" },
        { number: 9, ruta: "nine" },
        { number: 10, ruta: "ten" },
        { number: 11, ruta: "eleven" },
        { number: 12, ruta: "twelve" },
        { number: 13, ruta: "thirteen" },
        { number: 14, ruta: "fourteen" },
        { number: 15, ruta: "fifteen" },
        { number: 16, ruta: "sixteen" },
        { number: 17, ruta: "seventeen" },
        { number: 18, ruta: "eighteen" },
        { number: 19, ruta: "nineteen" },
        { number: 20, ruta: "twenty" }
      ],

      currentObject: {}
    };
  },

  methods: {
    crearAudio(sound) {
      console.log(sound.ruta, sound.number);
      var number = document.getElementById(sound.ruta);
      number.play();
    },

    cargarAudiosAleatorio() {
      let number = Math.floor(Math.random() * (21 - 0) + 0);

      this.arregloAudios.map(x => {
        if (x.number == number) {
          this.crearAudio(x);
          this.currentObject = { ...x };
        }
      });
    },

    async comprobar() {
      try {
        console.log("Hoola");
        console.log("Numero del input", this.text);
        console.log("Numero dicho de voz", this.currentObject.number);

        if (this.text === this.currentObject.number.toString()) {
          var number = document.getElementById("correct");
          await number.play();
          this.$q.notify({
            type: "positive",
            message: `Vas muy bien !!`
          });

          this.text = "";
        } else {
          var number = document.getElementById("incorrect");
          await number.play();

          this.$q.notify({
            type: "negative",
            message: `Try Again!!`
          });
        }
      } catch (error) {}
    },

    repeat() {
      this.crearAudio(this.currentObject);
    }
  }
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
