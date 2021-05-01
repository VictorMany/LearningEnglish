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
      Verbs
    </h4>

    <div>
      <audio id="1"><source src="verbs/1.mp3" /></audio>
      <audio id="2"><source src="verbs/2.mp3" /></audio>
      <audio id="3"><source src="verbs/3.mp3" /></audio>
      <audio id="4"><source src="verbs/4.mp3" /></audio>
      <audio id="5"><source src="verbs/5.mp3" /></audio>
      <audio id="6"><source src="verbs/6.mp3" /></audio>
      <audio id="7"><source src="verbs/7.mp3" /></audio>
      <audio id="8"><source src="verbs/8.mp3" /></audio>
      <audio id="9"><source src="verbs/9.mp3" /></audio>
      <audio id="10"><source src="verbs/10.mp3" /></audio>
      <audio id="11"><source src="verbs/11.mp3" /></audio>
      <audio id="12"><source src="verbs/12.mp3" /></audio>
      <audio id="13"><source src="verbs/13.mp3" /></audio>
      <audio id="14"><source src="verbs/14.mp3" /></audio>
      <audio id="15"><source src="verbs/15.mp3" /></audio>
      <audio id="16"><source src="verbs/16.mp3" /></audio>
      <audio id="17"><source src="verbs/17.mp3" /></audio>
      <audio id="18"><source src="verbs/18.mp3" /></audio>
      <audio id="19"><source src="verbs/19.mp3" /></audio>
      <audio id="20"><source src="verbs/20.mp3" /></audio>
      <audio id="21"><source src="verbs/21.mp3" /></audio>
      <audio id="22"><source src="verbs/22.mp3" /></audio>
      <audio id="23"><source src="verbs/23.mp3" /></audio>
      <audio id="24"><source src="verbs/24.mp3" /></audio>
      <audio id="25"><source src="verbs/25.mp3" /></audio>
      <audio id="26"><source src="verbs/26.mp3" /></audio>
      <audio id="27"><source src="verbs/27.mp3" /></audio>
      <audio id="28"><source src="verbs/28.mp3" /></audio>
      <audio id="29"><source src="verbs/29.mp3" /></audio>
      <audio id="30"><source src="verbs/30.mp3" /></audio>
      <audio id="31"><source src="verbs/31.mp3" /></audio>
      <audio id="32"><source src="verbs/32.mp3" /></audio>
      <audio id="33"><source src="verbs/33.mp3" /></audio>
      <audio id="34"><source src="verbs/34.mp3" /></audio>
      <audio id="35"><source src="verbs/35.mp3" /></audio>
      <audio id="36"><source src="verbs/36.mp3" /></audio>
      <audio id="37"><source src="verbs/37.mp3" /></audio>
      <audio id="38"><source src="verbs/38.mp3" /></audio>
      <audio id="39"><source src="verbs/39.mp3" /></audio>
      <audio id="40"><source src="verbs/40.mp3" /></audio>
      <audio id="41"><source src="verbs/41.mp3" /></audio>
      <audio id="42"><source src="verbs/42.mp3" /></audio>
      <audio id="43"><source src="verbs/43.mp3" /></audio>
      <audio id="44"><source src="verbs/44.mp3" /></audio>
      <audio id="45"><source src="verbs/45.mp3" /></audio>
      <audio id="46"><source src="verbs/46.mp3" /></audio>
      <audio id="47"><source src="verbs/47.mp3" /></audio>
      <audio id="48"><source src="verbs/48.mp3" /></audio>
      <audio id="49"><source src="verbs/49.mp3" /></audio>
      <audio id="50"><source src="verbs/50.mp3" /></audio>

      <audio id="correct"><source src="numbers/sounds/correct.mp3" /></audio>
      <audio id="incorrect">
        <source src="numbers/sounds/incorrect.mp3" />
      </audio>
    </div>

    <div>
      <q-btn
        style="
          width: 100%;
          height: auto;
          margin-top: -1rem;
          margin-bottom: 1rem;
        "
        push
        class="q-btn"
        @click="cargarAudiosAleatorio()"
        color="light-blue-13"
        icon="campaign"
      >
        <div class="row justify-center" style="width: 100%">CLICK ME !!</div>
        <p class="row justify-center text-white" style="font-size: 0.6rem">
          Haz click en mi !!
        </p>
      </q-btn>

      <div class="row justify-around" style="overflow: scroll">
        <q-btn
          push
          no-caps
          class="q-btn"
          v-for="(i, index) of arrayVerbs"
          v-bind:key="index"
          @click="comprobar(i.numero.toString())"
          style="width: 100%; background-color: rgb(0, 70, 150); color: white"
        >
          <div class="row justify-center text-h6" style="width: 100%">
            {{ i.phrase }}
          </div>
          <div class="row justify-center" style="width: 100%">
            <q-item-label style="font-size: 15px; color: grey">{{
              i.trad
            }}</q-item-label>
          </div>
        </q-btn>
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
            Si obtienes un rojo es que deberías de estudiar más los verbos
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
      text: "",
      ph: "",

      dense: false,
      arrayVerbs: [
        { numero: 1, phrase: "To speak", trad: "Hablar" },
        { numero: 2, phrase: "To eat", trad: "Comer" },
        { numero: 3, phrase: "To leave", trad: "Salir" },
        { numero: 4, phrase: "To live", trad: "Vivir" },
        { numero: 5, phrase: "To be", trad: "Ser/Estar" },
        { numero: 6, phrase: "To have", trad: "Tener" },
        { numero: 7, phrase: "To put", trad: "Poner" },
        { numero: 8, phrase: "To take", trad: "Tomar" },
        { numero: 9, phrase: "To give", trad: "Dar" },
        { numero: 10, phrase: "To go", trad: "Ir" },
        { numero: 11, phrase: "To say", trad: "Decir" },
        { numero: 12, phrase: "To make", trad: "Hacer" },
        { numero: 13, phrase: "To need", trad: "Necesitar" },
        { numero: 14, phrase: "To want", trad: "Querer" },
        { numero: 15, phrase: "To open", trad: "Abrir" },
        { numero: 16, phrase: "To grab", trad: "Agarrar/Tomar" },
        { numero: 17, phrase: "To walk", trad: "Caminar" },
        { numero: 18, phrase: "To drink", trad: "Tomar/Beber" },
        { numero: 19, phrase: "To close", trad: "Cerrar" },
        { numero: 20, phrase: "To start", trad: "Empezar/Comenzar" },
        { numero: 21, phrase: "To buy", trad: "Comprar" },
        { numero: 22, phrase: "To drive", trad: "Manejar/Conducir" },
        { numero: 23, phrase: "To know", trad: "Saber/Conocer" },
        { numero: 24, phrase: "To order", trad: "Ordenar" },
        { numero: 25, phrase: "To sleep", trad: "Dormir" },
        { numero: 26, phrase: "To find", trad: "Encontrar" },
        { numero: 27, phrase: "To unserstand", trad: "Entender" },
        { numero: 28, phrase: "To write", trad: "Escribir" },
        { numero: 29, phrase: "To think", trad: "Pensar" },
        { numero: 30, phrase: "To read", trad: "Leer" },
        { numero: 31, phrase: "To watch", trad: "Mirar" },
        { numero: 32, phrase: "To arrive", trad: "Llegar" },
        { numero: 33, phrase: "To search", trad: "Buscar" },
        { numero: 34, phrase: "To lose", trad: "Perder" },
        { numero: 35, phrase: "To hear", trad: "Oír" },
        { numero: 36, phrase: "To play", trad: "Jugar" },
        { numero: 37, phrase: "To jump", trad: "Saltar" },
        { numero: 38, phrase: "To see", trad: "Ver" },
        { numero: 39, phrase: "To work", trad: "Trabajar" },
        { numero: 40, phrase: "To bring", trad: "Traer" },
        { numero: 41, phrase: "To feel", trad: "Sentir" },
        { numero: 42, phrase: "To pay (for)", trad: "Pagar" },
        { numero: 43, phrase: "To begin", trad: "Empezar" },
        { numero: 44, phrase: "To choose", trad: "Elegir" },
        { numero: 45, phrase: "To fly", trad: "Volar" },
        { numero: 46, phrase: "To forget", trad: "Olvidar" },
        { numero: 47, phrase: "To get", trad: "Obtener" },
        { numero: 48, phrase: "To run", trad: "Correr" },
        { numero: 49, phrase: "To come", trad: "Venir" },
        { numero: 50, phrase: "To go", trad: "Ir" },
      ],
      currentObject: {},
    };
  },

  methods: {
    crearAudio(sound) {
      console.log(sound);
      var number = document.getElementById(sound);
      number.play();
    },
    cargarAudiosAleatorio() {
      console.log("Entro a los audios aleatorios");
      let number = Math.floor(Math.random() * (20 - 0) + 0);
      this.arrayVerbs.map((x) => {
        if (x.numero == number) {
          this.crearAudio(x.numero.toString());
          this.currentObject = { ...x };
        }
      });
    },
    async comprobar(text) {
      try {
        console.log("Numero del input", text);
        console.log(
          "Numero de comprobar",
          this.currentObject.numero.toString()
        );
        if (text.toLowerCase() === this.currentObject.numero.toString()) {
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
        this.crearAudio(this.currentObject.numero.toString());
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
