<template>
  <div class="q-pa-md" style="width: 100%">
    <div class="row">
      <div class="col-12">
        <q-btn style="width: 100%" color="blue" label="PROXIMAMENTE" />
      </div>
    </div>

    <q-dialog transition-show="rotate" transition-hide="rotate">
      <q-card>
        <q-card-section>
          <div class="text-h6">Sumar</div>
        </q-card-section>
        <q-card-section class="q-pt-none"> </q-card-section>

        <q-card-actions class="absolute-bottom">
          <q-btn flat label="Decline" color="primary" v-close-popup />
          <q-btn flat label="Accept" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
  </div>
</template>


<script>
export default {};
</script>

<style lang="sass" scoped>
button
  color: $blue
  padding: 0.3rem
  margin: 0.2rem
</style>