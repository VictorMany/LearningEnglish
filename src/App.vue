<template>
  <div id="q-app">
    <router-view />
  </div>
</template>
<script lang="ts">
import { defineComponent } from "@vue/composition-api";

export default defineComponent({
  name: "App",
});
</script>


<style>
::-webkit-scrollbar {
  margin-bottom: 0rem; /* remove default margin */
  scrollbar-width: none; /* Also needed to disable scrollbar Firefox */
  -ms-overflow-style: none; /* Disable scrollbar IE 10+ */
  overflow-y: scroll;
  width: 0px;
  background: transparent; /* Disable scrollbar Chrome/Safari/Webkit */
}
</style>