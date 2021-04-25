<template>
  <div style="width: 100%; height: 90%; overflow: scroll">
    <h4
      style="
        margin-top: 1rem;
        margin-bottom: 1rem;
        width: 100%;
        padding: 0.4rem;
        border-radius: 0.5rem;
        align: center;
        font-weight: bold;
      "
      class="bg-blue-13 text-white text-center"
    >
      Basic Phrases
    </h4>
    <div>
      <audio id="1"><source src="phrases/1.mp3" /></audio>
      <audio id="2"><source src="phrases/2.mp3" /></audio>
      <audio id="3"><source src="phrases/3.mp3" /></audio>
      <audio id="4"><source src="phrases/4.mp3" /></audio>
      <audio id="5"><source src="phrases/5.mp3" /></audio>
      <audio id="6"><source src="phrases/6.mp3" /></audio>
      <audio id="7"><source src="phrases/7.mp3" /></audio>
      <audio id="8"><source src="phrases/8.mp3" /></audio>
      <audio id="9"><source src="phrases/9.mp3" /></audio>
      <audio id="10"><source src="phrases/10.mp3" /></audio>
      <audio id="11"><source src="phrases/11.mp3" /></audio>
      <audio id="12"><source src="phrases/12.mp3" /></audio>
      <audio id="13"><source src="phrases/13.mp3" /></audio>
      <audio id="14"><source src="phrases/14.mp3" /></audio>
      <audio id="15"><source src="phrases/15.mp3" /></audio>
      <audio id="16"><source src="phrases/16.mp3" /></audio>
      <audio id="17"><source src="phrases/17.mp3" /></audio>
      <audio id="18"><source src="phrases/18.mp3" /></audio>
      <audio id="19"><source src="phrases/19.mp3" /></audio>
      <audio id="20"><source src="phrases/20.mp3" /></audio>
    </div>

    <div>
      <div class="row justify-around" style="overflow: scroll">
        <q-btn
          push
          no-caps
          class="q-btn"
          v-for="(i, index) of arrayPhrases"
          v-bind:key="index"
          @click="crearAudio(i.numero.toString())"
          style="width: 100%; background-color: rgb(30, 30, 150); color: white"
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
  </div>
</template>

<script>
export default {
  data() {
    return {
      arrayPhrases: [
        { numero: 1, phrase: "Hello", trad: "Hola" },
        { numero: 2, phrase: "Yes", trad: "Si" },
        { numero: 3, phrase: "No", trad: "No" },
        { numero: 4, phrase: "How are you?", trad: "¿Cómo estás?" },
        { numero: 5, phrase: "What´s Up", trad: "¿Qué pasa? (Saludo)" },
        { numero: 6, phrase: "Thank you", trad: "Gracias" },
        { numero: 7, phrase: "Please", trad: "Por favor" },
        { numero: 8, phrase: "You´re welcome", trad: "De nada" },
        { numero: 9, phrase: "Excuse me", trad: "Discúlpame" },
        { numero: 10, phrase: "Good morning", trad: "Buenos días" },
        { numero: 11, phrase: "Good afternoon", trad: "Buenas tardes" },
        {
          numero: 12,
          phrase: "Good evening",
          trad: "Buenas noches (tarde-noche)",
        },
        { numero: 13, phrase: "Good night", trad: "Buenas noches" },
        {
          numero: 14,
          phrase: "Do you speak Spanish?",
          trad: "¿Hablas Español?",
        },
        {
          numero: 15,
          phrase: "Mi name is Martín",
          trad: "Mi nombre es Martín",
        },
        { numero: 16, phrase: "This is Laura", trad: "ésta es Laura" },
        { numero: 17, phrase: "How have you been?", trad: "¿Cómo has estado?" },
        {
          numero: 18,
          phrase: "I´m fine, thank you",
          trad: "Estoy bien, gracias",
        },
        { numero: 19, phrase: "What did you say?", trad: "¿Qué dijiste?" },
        {
          numero: 20,
          phrase: "Have a nice day! ",
          trad: "Que tenga un buen día!",
        },
      ],
    };
  },

  methods: {
    crearAudio(sound) {
      try {
        sound = sound.toLowerCase();
        console.log(sound);
        var audio = document.getElementById(sound);
        audio.play();
      } catch (error) {
        console.log(error);
      }
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
  width: 90%
  height: 70px
  margin-bottom: 0.5rem
  padding-top: 0.3rem
  font-size: 1.3rem

.q-btn_mitad
  width: 47%
  height: 70px
  margin-bottom: 0.5rem
  padding-top: 0.3rem

h6
  margin-top: -0.5rem

.qScrollStyle
  height: 100%
  width: 100%
</style>
