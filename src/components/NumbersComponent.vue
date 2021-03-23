<template>
  <div class="q-pa-md" style="width: 100% ">
    <div class="row">
      <div class="col-12" style="margin-top: -1rem">
        <q-btn
          class="button"
          style="width: 100%"
          color="blue"
          push
          label="Numbers (0-20)"
          @click="numbers_0_20 = true"
        >
          <p style="font-size: 0.7rem" class="text-grey-5 col-12">
            (Números del 0 al 20)
          </p></q-btn
        >
        <q-btn
          push
          class="button"
          style="width: 100%"
          color="blue"
          label="Numbers (Tens)"
          @click="numbers_tens = true"
        >
          <p style="font-size: 0.7rem" class="text-grey-5 col-12">
            (Números en decenas)
          </p></q-btn
        >
        <q-btn
          push
          class="button"
          style="width: 100%"
          color="blue"
          label="Numbers (Hundreds)"
          @click="numbers_hundreds = true"
        >
          <p style="font-size: 0.7rem" class="text-grey-5 col-12">
            (Números en centenas)
          </p></q-btn
        >
        <q-btn
          push
          style="width: 100%"
          class="button"
          color="blue"
          label="Numbers (Thousand units)"
          @click="numbers_thousands = true"
        >
          <p style="font-size: 0.7rem" class="text-grey-5 col-12">
            (Numeros en Unidades de mil)
          </p>
        </q-btn>  
      </div>
    </div>

    <q-dialog
      v-model="numbers_0_20"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <q-card
        style="width: 100%;  background-color: rgb(10, 10, 10, 0.85); overflow: scroll"
      >
        <q-card-section
          class="bg-blue-10 text-white"
          style="border-radius: 0.5rem; margin: 1rem"
        >
          <div class="text-h6">
            <h6>Numbers from 0 to 20</h6>
            <p style="font-size: 1rem; margin-top: -3rem; color: grey">
              (Números del 0 al 20)
            </p>
          </div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <!--AAQUI VAMOS A PONER NUESTRO GUTTER CON LOS NUMEROS DEL 1 AL 10 CON BOTONES-->

          <div class="row justify-around" style="margin-bottom: 2rem">
            <q-btn
              push
              class="q-btn"
              @click="crearAudio('zero')"
              color="green-10"
            >
              <div class="row justify-center" style="width: 100%">Zero</div>
              <p class="row justify-center text-white">0</p></q-btn
            >
            <q-btn
              push
              class="q-btn"
              @click="crearAudio('one')"
              color="green-10"
            >
              <div class="row justify-center" style="width: 100%">One</div>
              <p class="row justify-center text-white">1</p></q-btn
            >

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

            <q-btn
              push
              class="q-btn"
              color="green-10"
              @click="crearAudio('two')"
            >
              <div class="row justify-center" style="width: 100%">Two</div>
              <p class="row justify-center text-white">2</p></q-btn
            >

            <q-btn
              push
              class="q-btn"
              @click="crearAudio('three')"
              color="green-9"
            >
              <div class="row justify-center" style="width: 100%">Three</div>
              <p class="row justify-center text-white">3</p></q-btn
            >
            <q-btn
              push
              class="q-btn"
              @click="crearAudio('four')"
              color="green-9"
            >
              <div class="row justify-center" style="width: 100%">Four</div>
              <p class="row justify-center text-white">4</p></q-btn
            >
            <q-btn
              push
              class="q-btn"
              @click="crearAudio('five')"
              color="green-9"
            >
              <div class="row justify-center" style="width: 100%">Five</div>
              <p class="row justify-center text-white">5</p></q-btn
            >
            <q-btn
              push
              class="q-btn"
              @click="crearAudio('six')"
              color="green-8"
            >
              <div class="row justify-center" style="width: 100%">Six</div>
              <p class="row justify-center text-white">6</p></q-btn
            >
            <q-btn
              push
              class="q-btn"
              @click="crearAudio('seven')"
              color="green-8"
            >
              <div class="row justify-center" style="width: 100%">Seven</div>
              <p class="row justify-center text-white">7</p></q-btn
            >
            <q-btn
              push
              class="q-btn"
              @click="crearAudio('eight')"
              color="green-8"
            >
              <div class="row justify-center" style="width: 100%">Eight</div>
              <p class="row justify-center text-white">8</p></q-btn
            >
            <q-btn
              push
              class="q-btn"
              @click="crearAudio('nine')"
              color="green-7"
            >
              <div class="row justify-center" style="width: 100%">Nine</div>
              <p class="row justify-center text-white">9</p></q-btn
            >
            <q-btn
              push
              class="q-btn"
              @click="crearAudio('ten')"
              color="green-7"
            >
              <div class="row justify-center" style="width: 100%">Ten</div>
              <p class="row justify-center text-white">10</p></q-btn
            >

            <q-btn
              push
              class="q-btn"
              @click="crearAudio('eleven')"
              color="green-7"
            >
              <div class="row justify-center" style="width: 100%">Eleven</div>
              <p class="row justify-center text-white">11</p></q-btn
            >

            <q-btn
              push
              class="q-btn"
              @click="crearAudio('twelve')"
              color="green-6"
            >
              <div class="row justify-center" style="width: 100%">Twelve</div>
              <p class="row justify-center text-white">12</p></q-btn
            >

            <q-btn
              push
              class="q-btn"
              @click="crearAudio('thirteen')"
              color="green-6"
            >
              <div class="row justify-center" style="width: 100%">Thirteen</div>
              <p class="row justify-center text-white">13</p></q-btn
            >

            <q-btn
              push
              class="q-btn"
              @click="crearAudio('fourteen')"
              color="green-6"
            >
              <div class="row justify-center" style="width: 100%">Fourteen</div>
              <p class="row justify-center text-white">14</p></q-btn
            >

            <q-btn
              push
              class="q-btn"
              @click="crearAudio('fifteen')"
              color="green-6"
            >
              <div class="row justify-center" style="width: 100%">Fifteen</div>
              <p class="row justify-center text-white">15</p></q-btn
            >

            <q-btn
              push
              class="q-btn"
              @click="crearAudio('sixteen')"
              color="green-6"
            >
              <div class="row justify-center" style="width: 100%">Sixteen</div>
              <p class="row justify-center text-white">16</p></q-btn
            >

            <q-btn
              push
              class="q-btn"
              @click="crearAudio('seventeen')"
              color="green-6"
            >
              <div class="row justify-center" style="width: 100%">
                Seventeen
              </div>
              <p class="row justify-center text-white">17</p></q-btn
            >

            <q-btn
              push
              class="q-btn"
              @click="crearAudio('eighteen')"
              color="green-6"
            >
              <div class="row justify-center" style="width: 100%">Eighteen</div>
              <p class="row justify-center text-white">18</p></q-btn
            >

            <q-btn
              push
              class="q-btn"
              @click="crearAudio('nineteen')"
              color="green-6"
            >
              <div class="row justify-center" style="width: 100%">Nineteen</div>
              <p class="row justify-center text-white">19</p></q-btn
            >

            <q-btn
              push
              class="q-btn"
              @click="crearAudio('twenty')"
              color="green-6"
            >
              <div class="row justify-center" style="width: 100%">Twenty</div>
              <p class="row justify-center text-white">20</p></q-btn
            >
          </div>
        </q-card-section>
        <q-card-actions>
          <q-btn
            style="height: 100%; width: 100%"
            push
            label="Close"
            color="red-10"
            v-close-popup
          ></q-btn>
        </q-card-actions>
      </q-card>
    </q-dialog>

    <q-dialog
      v-model="numbers_tens"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <q-card
        style="width: 100%;  background-color: rgb(10, 10, 10, 0.85); overflow: scroll"
      >
        <q-card-section
          class="bg-blue-10 text-white"
          style="border-radius: 0.5rem; margin: 1rem"
        >
          <div class="text-h6">
            <h6>Numbers from 10 to 100</h6>
            <p style="font-size: 1rem; margin-top: -3rem; color: grey">
              (Números del 10 al 100)
            </p>
          </div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <!--AAQUI VAMOS A PONER NUESTRO GUTTER CON LOS NUMEROS DEL 1 AL 10 CON BOTONES-->

          <div class="row justify-around" style="margin-bottom: 2rem">
            <audio id="ten"><source src="numbers/ten.mp3" /></audio>
            <audio id="twenty"><source src="numbers/twenty.mp3" /></audio>
            <audio id="thirty">
              <source src="numbers/tens/fourty.mp3" />
            </audio>
            <audio id="fourty">
              <source src="numbers/tens/thirty.mp3" />
            </audio>
            <audio id="fifty"><source src="numbers/tens/fifty.mp3" /></audio>
            <audio id="sixty"><source src="numbers/tens/sixty.mp3" /></audio>
            <audio id="seventy">
              <source src="numbers/tens/seventy.mp3" />
            </audio>
            <audio id="eighty">
              <source src="numbers/tens/eighty.mp3" />
            </audio>
            <audio id="ninty">
              <source src="numbers/tens/onehundred.mp3" />
            </audio>
            <audio id="onehundred">
              <source src="numbers/tens/ninety.mp3" />
            </audio>

            <q-btn
              push
              class="q-btn_mitad"
              color="purple-10"
              @click="crearAudio('ten')"
            >
              <div class="row justify-center" style="width: 100%">Ten</div>
              <p class="row justify-center text-white">10</p></q-btn
            >

            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('twenty')"
              color="purple-10"
            >
              <div class="row justify-center" style="width: 100%">Twenty</div>
              <p class="row justify-center text-white">20</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('thirty')"
              color="purple-9"
            >
              <div class="row justify-center" style="width: 100%">Thirty</div>
              <p class="row justify-center text-white">30</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('fourty')"
              color="purple-9"
            >
              <div class="row justify-center" style="width: 100%">Fourty</div>
              <p class="row justify-center text-white">40</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('fifty')"
              color="purple-8"
            >
              <div class="row justify-center" style="width: 100%">Fifty</div>
              <p class="row justify-center text-white">50</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('sixty')"
              color="purple-8"
            >
              <div class="row justify-center" style="width: 100%">Sixty</div>
              <p class="row justify-center text-white">60</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('seventy')"
              color="purple-7"
            >
              <div class="row justify-center" style="width: 100%">Seventy</div>
              <p class="row justify-center text-white">70</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('eighty')"
              color="purple-7"
            >
              <div class="row justify-center" style="width: 100%">Eighty</div>
              <p class="row justify-center text-white">80</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('ninty')"
              color="purple-6"
            >
              <div class="row justify-center" style="width: 100%">Ninety</div>
              <p class="row justify-center text-white">90</p></q-btn
            >

            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('onehundred')"
              color="purple-6"
            >
              <div class="row justify-center" style="width: 100%">
                One Hundred
              </div>
              <p class="row justify-center text-white">100</p></q-btn
            >
          </div>
        </q-card-section>
        <q-card-actions>
          <q-btn
            style="height: 100%; width: 100%"
            push
            label="Close"
            color="red-10"
            v-close-popup
          ></q-btn>
        </q-card-actions>
      </q-card>
    </q-dialog>

    <q-dialog
      v-model="numbers_hundreds"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <q-card
        style="width: 100%;  background-color: rgb(10, 10, 10, 0.85); overflow: scroll"
      >
        <q-card-section
          class="bg-blue-10 text-white"
          style="border-radius: 0.5rem; margin: 1rem"
        >
          <div class="text-h6">
            <h6>Numbers from 100 to 1000</h6>
            <p style="font-size: 1rem; margin-top: -3rem; color: grey">
              (Números del 100 al 1000)
            </p>
          </div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <!--AAQUI VAMOS A PONER NUESTRO GUTTER CON LOS NUMEROS DEL 1 AL 10 CON BOTONES-->

          <div class="row justify-around" style="margin-bottom: 2rem">
            <audio id="100"><source src="numbers/hundreds/100.mp3" /></audio>
            <audio id="200"><source src="numbers/hundreds/200.mp3" /></audio>
            <audio id="300">
              <source src="numbers/hundreds/300.mp3" />
            </audio>
            <audio id="400">
              <source src="numbers/hundreds/400.mp3" />
            </audio>
            <audio id="500"><source src="numbers/hundreds/500.mp3" /></audio>
            <audio id="600"><source src="numbers/hundreds/600.mp3" /></audio>
            <audio id="700">
              <source src="numbers/hundreds/700.mp3" />
            </audio>
            <audio id="800">
              <source src="numbers/hundreds/800.mp3" />
            </audio>
            <audio id="900">
              <source src="numbers/hundreds/900.mp3" />
            </audio>
            <audio id="1000">
              <source src="numbers/hundreds/1000.mp3" />
            </audio>

            <q-btn
              push
              class="q-btn_mitad"
              color="indigo-10"
              @click="crearAudio('100')"
            >
              <div class="row justify-center" style="width: 100%">
                One Hundred
              </div>
              <p class="row justify-center text-white">100</p></q-btn
            >

            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('200')"
              color="indigo-10"
            >
              <div class="row justify-center" style="width: 100%">
                Two Hundred
              </div>
              <p class="row justify-center text-white">200</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('300')"
              color="indigo-9"
            >
              <div class="row justify-center" style="width: 100%">
                Three Hundred
              </div>
              <p class="row justify-center text-white">300</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('400')"
              color="indigo-9"
            >
              <div class="row justify-center" style="width: 100%">
                Four Hundred
              </div>
              <p class="row justify-center text-white">400</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('500')"
              color="indigo-8"
            >
              <div class="row justify-center" style="width: 100%">
                Five Hundred
              </div>
              <p class="row justify-center text-white">500</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('600')"
              color="indigo-8"
            >
              <div class="row justify-center" style="width: 100%">
                Six Hundred
              </div>
              <p class="row justify-center text-white">600</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('700')"
              color="indigo-7"
            >
              <div class="row justify-center" style="width: 100%">
                Seven Hundred
              </div>
              <p class="row justify-center text-white">700</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('800')"
              color="indigo-7"
            >
              <div class="row justify-center" style="width: 100%">
                Eight Hundred
              </div>
              <p class="row justify-center text-white">800</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('900')"
              color="indigo-6"
            >
              <div class="row justify-center" style="width: 100%">
                Nine Hundred
              </div>
              <p class="row justify-center text-white">900</p></q-btn
            >

            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('1000')"
              color="indigo-6"
            >
              <div class="row justify-center" style="width: 100%">
                One Thounsand
              </div>
              <p class="row justify-center text-white">1000</p></q-btn
            >
          </div>
        </q-card-section>
        <q-card-actions>
          <q-btn
            style="height: 100%; width: 100%"
            push
            label="Close"
            color="red-10"
            v-close-popup
          ></q-btn>
        </q-card-actions>
      </q-card>
    </q-dialog>

   <q-dialog
      v-model="numbers_thousands"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <q-card
        style="width: 100%;  background-color: rgb(10, 10, 10, 0.85); overflow: scroll"
      >
        <q-card-section
          class="bg-blue-10 text-white"
          style="border-radius: 0.5rem; margin: 1rem"
        >
          <div class="text-h6">
            <h6>Numbers from 1000 to 10000</h6>
            <p style="font-size: 1rem; margin-top: -3rem; color: grey">
              (Números del 1000 al 10000)
            </p>
          </div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <!--AAQUI VAMOS A PONER NUESTRO GUTTER CON LOS NUMEROS DEL 1 AL 10 CON BOTONES-->

          <div class="row justify-around" style="margin-bottom: 2rem">
            <audio id="1000"><source src="numbers/thousands/1000.mp3" /></audio>
            <audio id="2000"><source src="numbers/thousands/2000.mp3" /></audio>
            <audio id="3000">
              <source src="numbers/thousands/3000.mp3" />
            </audio>
            <audio id="4000">
              <source src="numbers/thousands/4000.mp3" />
            </audio>
            <audio id="5000"><source src="numbers/thousands/5000.mp3" /></audio>
            <audio id="6000"><source src="numbers/thousands/6000.mp3" /></audio>
            <audio id="7000">
              <source src="numbers/thousands/7000.mp3" />
            </audio>
            <audio id="8000">
              <source src="numbers/thousands/8000.mp3" />
            </audio>
            <audio id="9000">
              <source src="numbers/thousands/9000.mp3" />
            </audio>
            <audio id="10000">
              <source src="numbers/thousands/10000.mp3" />
            </audio>

            <q-btn
              push
              class="q-btn_mitad"
              color="pink-10"
              @click="crearAudio('1000')"
            >
              <div class="row justify-center" style="width: 100%">
                One Thousand
              </div>
              <p class="row justify-center text-white">1000</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('2000')"
              color="pink-10"
            >
              <div class="row justify-center" style="width: 100%">
                Two Thousand
              </div>
              <p class="row justify-center text-white">2000</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('3000')"
              color="pink-9"
            >
              <div class="row justify-center" style="width: 100%">
                Three Thousand
              </div>
              <p class="row justify-center text-white">3000</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('4000')"
              color="pink-9"
            >
              <div class="row justify-center" style="width: 100%">
                Four Thousand
              </div>
              <p class="row justify-center text-white">4000</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('5000')"
              color="pink-8"
            >
              <div class="row justify-center" style="width: 100%">
                Five Thousand
              </div>
              <p class="row justify-center text-white">5000</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('6000')"
              color="pink-8"
            >
              <div class="row justify-center" style="width: 100%">
                Six Thousand
              </div>
              <p class="row justify-center text-white">6000</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('7000')"
              color="pink-7"
            >
              <div class="row justify-center" style="width: 100%">
                Seven Thousand
              </div>
              <p class="row justify-center text-white">7000</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('8000')"
              color="pink-7"
            >
              <div class="row justify-center" style="width: 100%">
                Eight Thousand
              </div>
              <p class="row justify-center text-white">8000</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('9000')"
              color="pink-6"
            >
              <div class="row justify-center" style="width: 100%">
                Nine Thousand
              </div>
              <p class="row justify-center text-white">9000</p></q-btn
            >
            <q-btn
              push
              class="q-btn_mitad"
              @click="crearAudio('10000')"
              color="pink-6"
            >
              <div class="row justify-center" style="width: 100%">
                Ten Thounsand
              </div>
              <p class="row justify-center text-white">10000</p></q-btn
            >
          </div>

        </q-card-section>
        <q-card-actions>
          <q-btn
            style="height: 100%; width: 100%"
            push
            label="Close"
            color="red-10"
            v-close-popup
          ></q-btn>
        </q-card-actions>
      </q-card>
    </q-dialog>
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
      thumbStyle: {
        right: "-6px",
        borderRadius: "1px",
        backgroundColor: "#027be3",
        width: "2px",
        opacity: 0.75
      },
      barStyle: {
        right: "-6px",
        borderRadius: "9px",
        backgroundColor: "#027be3",
        width: "2px",
        opacity: 0.2
      }
    };
  },

  methods: {
    crearAudio(sound) {
      var number = document.getElementById(sound);
      number.play();
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
  height: auto
  margin-bottom: 0.5rem
  padding-top: 0.3rem

h6
  margin-top: -0.5rem

.qScrollStyle
  height: 100%
  width: 100%
</style>
