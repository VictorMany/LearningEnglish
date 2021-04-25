<template>
  <q-card
    class="my-card row justify-center"
    style="background-color: rgb(0, 0, 0, 0)"
  >
    <!--  DIV DE LOS AUDIOS-->
    <div>
      <audio id="i"><source src="pronouns/i.mp3" /></audio>
      <audio id="you"><source src="pronouns/you.mp3" /></audio>
      <audio id="they"><source src="pronouns/they.mp3" /></audio>
      <audio id="we"><source src="pronouns/we.mp3" /></audio>
      <audio id="she"><source src="pronouns/she.mp3" /></audio>
      <audio id="he"><source src="pronouns/he.mp3" /></audio>
      <audio id="it"><source src="pronouns/it.mp3" /></audio>
    </div>
    <!--  DIV DE LOS AUDIOS-->
    <q-img
      style="width: 250px; height: 250px; border-radius: 10%"
      :src="imagen"
      basic
      class="row justify-center"
    >
      <div class="absolute-bottom column justify-center">
        <div class="text-h6 row justify-center">
          <strong :class="'text-' + color + ' text-center'">{{
            textoIngles
          }}</strong>
        </div>
        <p class="text-center text-bold">{{ textoEspaniol }}</p>
        <q-btn
          @click="crearAudio(audio)"
          class="self-center shadow-24"
          :color="color"
          push
          icon="campaign"
          :class="color === 'white' ? 'text-black' : 'text-white'"
        ></q-btn>
      </div>
    </q-img>
  </q-card>
</template>

<script>
export default {
  data() {
    return {};
  },

  methods: {
    crearAudio(sound) {
      var number = document.getElementById(sound.toLowerCase());
      console.log(sound);

      number.play();
    },
  },

  props: {
    imagen: {
      type: String,
      required: true,
      default: "img_pronouns/i.png",
    },

    color: {
      type: String,
      default: "text-white",
    },

    textoIngles: {
      type: String,
      default: "The cat is GRAY",
    },

    textoEspaniol: {
      type: String,
      default: "El gato es gris",
    },

    audio: {
      type: String,
      default: "grey",
    },
  },
};
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 250px
</style>
