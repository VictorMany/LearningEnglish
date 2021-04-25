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
      Alphabet
    </h4>

    <div>
      <audio id="a"><source src="abc/a.mp3" /></audio>
      <audio id="b"><source src="abc/b.mp3" /></audio>
      <audio id="c"><source src="abc/c.mp3" /></audio>
      <audio id="d"><source src="abc/d.mp3" /></audio>
      <audio id="e"><source src="abc/e.mp3" /></audio>
      <audio id="f"><source src="abc/f.mp3" /></audio>
      <audio id="g"><source src="abc/g.mp3" /></audio>
      <audio id="h"><source src="abc/h.mp3" /></audio>
      <audio id="i"><source src="abc/i.mp3" /></audio>
      <audio id="j"><source src="abc/j.mp3" /></audio>
      <audio id="k"><source src="abc/k.mp3" /></audio>
      <audio id="l"><source src="abc/l.mp3" /></audio>
      <audio id="m"><source src="abc/m.mp3" /></audio>
      <audio id="n"><source src="abc/n.mp3" /></audio>
      <audio id="o"><source src="abc/o.mp3" /></audio>
      <audio id="p"><source src="abc/p.mp3" /></audio>
      <audio id="q"><source src="abc/q.mp3" /></audio>
      <audio id="r"><source src="abc/r.mp3" /></audio>
      <audio id="s"><source src="abc/s.mp3" /></audio>
      <audio id="t"><source src="abc/t.mp3" /></audio>
      <audio id="u"><source src="abc/u.mp3" /></audio>
      <audio id="v"><source src="abc/v.mp3" /></audio>
      <audio id="w"><source src="abc/w.mp3" /></audio>
      <audio id="x"><source src="abc/x.mp3" /></audio>
      <audio id="y"><source src="abc/y.mp3" /></audio>
      <audio id="z"><source src="abc/z.mp3" /></audio>
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

      <div class="row justify-around">
        <q-btn push class="q-btn" @click="comprobar('A')" color="pink-9"
          ><div class="row justify-center" style="width: 100%">A</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('B')" color="pink-9"
          ><div class="row justify-center" style="width: 100%">B</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('C')" color="pink-9"
          ><div class="row justify-center" style="width: 100%">C</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('D')" color="pink-9"
          ><div class="row justify-center" style="width: 100%">D</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('E')" color="pink-9"
          ><div class="row justify-center" style="width: 100%">E</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('F')" color="pink-9"
          ><div class="row justify-center" style="width: 100%">F</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('G')" color="pink-8"
          ><div class="row justify-center" style="width: 100%">G</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('H')" color="pink-8"
          ><div class="row justify-center" style="width: 100%">H</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('I')" color="pink-8"
          ><div class="row justify-center" style="width: 100%">I</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('J')" color="pink-8"
          ><div class="row justify-center" style="width: 100%">J</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('K')" color="pink-8"
          ><div class="row justify-center" style="width: 100%">K</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('L')" color="pink-8"
          ><div class="row justify-center" style="width: 100%">L</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('M')" color="pink-7"
          ><div class="row justify-center" style="width: 100%">M</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('N')" color="pink-7"
          ><div class="row justify-center" style="width: 100%">N</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('O')" color="pink-7"
          ><div class="row justify-center" style="width: 100%">O</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('P')" color="pink-7"
          ><div class="row justify-center" style="width: 100%">P</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('Q')" color="pink-7"
          ><div class="row justify-center" style="width: 100%">Q</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('R')" color="pink-7"
          ><div class="row justify-center" style="width: 100%">R</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('S')" color="pink-6"
          ><div class="row justify-center" style="width: 100%">S</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('T')" color="pink-6"
          ><div class="row justify-center" style="width: 100%">T</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('U')" color="pink-6"
          ><div class="row justify-center" style="width: 100%">U</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('V')" color="pink-8"
          ><div class="row justify-center" style="width: 100%">V</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('W')" color="pink-8"
          ><div class="row justify-center" style="width: 100%">W</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('X')" color="pink-8"
          ><div class="row justify-center" style="width: 100%">X</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('Y')" color="pink-9"
          ><div class="row justify-center" style="width: 100%">Y</div></q-btn
        >
        <q-btn push class="q-btn" @click="comprobar('Z')" color="pink-9"
          ><div class="row justify-center" style="width: 100%">Z</div></q-btn
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
            Si obtienes un rojo es que deberías de estudiar más el Abecedario
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
      arregloAudios: [
        { letra: 0, ruta: "a" },
        { letra: 1, ruta: "b" },
        { letra: 2, ruta: "c" },
        { letra: 3, ruta: "d" },
        { letra: 4, ruta: "e" },
        { letra: 5, ruta: "f" },
        { letra: 6, ruta: "g" },
        { letra: 7, ruta: "h" },
        { letra: 8, ruta: "i" },
        { letra: 9, ruta: "j" },
        { letra: 10, ruta: "k" },
        { letra: 11, ruta: "l" },
        { letra: 12, ruta: "m" },
        { letra: 13, ruta: "n" },
        { letra: 14, ruta: "o" },
        { letra: 15, ruta: "p" },
        { letra: 16, ruta: "q" },
        { letra: 17, ruta: "r" },
        { letra: 18, ruta: "s" },
        { letra: 19, ruta: "t" },
        { letra: 20, ruta: "u" },
        { letra: 21, ruta: "v" },
        { letra: 22, ruta: "w" },
        { letra: 23, ruta: "x" },
        { letra: 24, ruta: "y" },
        { letra: 25, ruta: "z" },
      ],

      currentObject: {},
    };
  },

  methods: {
    crearAudio(sound) {
      console.log(sound.ruta, sound.letra);
      var number = document.getElementById(sound.ruta);
      number.play();
    },

    cargarAudiosAleatorio() {
      console.log("Entro a los audios aleatorios");
      let number = Math.floor(Math.random() * (26 - 0) + 0);
      this.arregloAudios.map((x) => {
        if (x.letra == number) {
          this.crearAudio(x);
          this.currentObject = { ...x };
        }
      });
    },

    async comprobar(text) {
      try {
        console.log("Hoola");
        console.log("Numero del input", text);
        console.log("Numero de comprobar", this.currentObject.ruta);

        if (text.toLowerCase() === this.currentObject.ruta.toLowerCase()) {
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
        this.crearAudio(this.currentObject);
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
