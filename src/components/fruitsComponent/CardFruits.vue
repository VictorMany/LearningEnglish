<template>
  <q-card
    class="my-card row bg-white"
    style="background-color: rgb(0,0,0,0.0); width: 100%, height: 100%; border-radius: 10%;"
  >
    <audio id="1"><source src="fruit/1.mp3" /></audio>
    <audio id="2"><source src="fruit/2.mp3" /></audio>
    <audio id="3"><source src="fruit/3.mp3" /></audio>
    <audio id="4"><source src="fruit/4.mp3" /></audio>
    <audio id="5"><source src="fruit/5.mp3" /></audio>
    <audio id="6"><source src="fruit/6.mp3" /></audio>
    <audio id="7"><source src="fruit/7.mp3" /></audio>
    <audio id="8"><source src="fruit/8.mp3" /></audio>
    <audio id="9"><source src="fruit/9.mp3" /></audio>
    <audio id="10"><source src="fruit/10.mp3" /></audio>
    <audio id="11"><source src="fruit/11.mp3" /></audio>
    <audio id="12"><source src="fruit/12.mp3" /></audio>
    <audio id="13"><source src="fruit/13.mp3" /></audio>
    <audio id="14"><source src="fruit/14.mp3" /></audio>
    <audio id="15"><source src="fruit/15.mp3" /></audio>
    <audio id="16"><source src="fruit/16.mp3" /></audio>

    <q-img
      style="border-radius: 10%"
      :src="imagen"
      basic
      :ratio="1"
      class="row justify-center"
    >
      <div
        v-if="textoEspaniol"
        class="fixed-bottom column justify-center"
        style="margin-bottom: -0.6rem"
      >
        <div class="text-p text-center" style="overflow: scroll">
          <strong class="text-yellow">{{ textoIngles }}</strong>
        </div>
        <p style="width: 100%; margin-bottom: 0.2rem" class="text-center">
          {{ textoEspaniol }}
        </p>
        <q-btn
          v-if="textoEspaniol != ''"
          @click="crearAudio(audio)"
          class="self-center shadow-24"
          :color="color"
          push
          size="sm"
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
      var number = document.getElementById(sound);
      number.play();
      console.log(sound);
    },
  },

  //Prop validators
  props: {
    imagen: {
      type: String,
      required: true,
      default: "img/colors_grey.jpg",
    },

    color: {
      type: String,
      default: "text-white",
      required: false,
    },

    textoIngles: {
      type: String,
      default: "",
      required: false,
    },

    textoEspaniol: {
      type: String,
      default: "",
      required: false,
    },

    audio: {
      type: Number,
      default: 1,
      required: false,
    },
  },
};
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 250px
</style>
