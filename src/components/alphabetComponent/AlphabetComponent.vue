<template>
  <div style="width: 100%; height: 90%;  overflow: scroll">
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
    </div>

    <div>
      <div class="row justify-around">
        <q-btn push class="q-btn" @click="crearAudio('A')" color="purple-9"
          ><div class="row justify-center" style="width: 100%">A</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('B')" color="purple-9"
          ><div class="row justify-center" style="width: 100%">B</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('C')" color="purple-9"
          ><div class="row justify-center" style="width: 100%">C</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('D')" color="purple-9"
          ><div class="row justify-center" style="width: 100%">D</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('E')" color="purple-9"
          ><div class="row justify-center" style="width: 100%">E</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('F')" color="purple-9"
          ><div class="row justify-center" style="width: 100%">F</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('G')" color="purple-8"
          ><div class="row justify-center" style="width: 100%">G</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('H')" color="purple-8"
          ><div class="row justify-center" style="width: 100%">H</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('I')" color="purple-8"
          ><div class="row justify-center" style="width: 100%">I</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('J')" color="purple-8"
          ><div class="row justify-center" style="width: 100%">J</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('K')" color="purple-8"
          ><div class="row justify-center" style="width: 100%">K</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('L')" color="purple-8"
          ><div class="row justify-center" style="width: 100%">L</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('M')" color="purple-7"
          ><div class="row justify-center" style="width: 100%">M</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('N')" color="purple-7"
          ><div class="row justify-center" style="width: 100%">N</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('O')" color="purple-7"
          ><div class="row justify-center" style="width: 100%">O</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('P')" color="purple-7"
          ><div class="row justify-center" style="width: 100%">P</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('Q')" color="purple-7"
          ><div class="row justify-center" style="width: 100%">Q</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('R')" color="purple-7"
          ><div class="row justify-center" style="width: 100%">R</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('S')" color="purple-6"
          ><div class="row justify-center" style="width: 100%">S</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('T')" color="purple-6"
          ><div class="row justify-center" style="width: 100%">T</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('U')" color="purple-6"
          ><div class="row justify-center" style="width: 100%">U</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('V')" color="purple-8"
          ><div class="row justify-center" style="width: 100%">V</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('W')" color="purple-8"
          ><div class="row justify-center" style="width: 100%">W</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('X')" color="purple-8"
          ><div class="row justify-center" style="width: 100%">X</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('Y')" color="purple-9"
          ><div class="row justify-center" style="width: 100%">Y</div></q-btn
        >
        <q-btn push class="q-btn" @click="crearAudio('Z')" color="purple-9"
          ><div class="row justify-center" style="width: 100%">Z</div></q-btn
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
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
  font-size: 1.3rem

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
