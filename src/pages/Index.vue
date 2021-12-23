<template>
  <q-page style="background-color: #1575A1;"  class="row items-center justify-center">
    <example-component
      title="Example component"
      active
    ></example-component>
  </q-page>
</template>

<script lang="ts">
import ExampleComponent from "components/CompositionComponent.vue";
import { defineComponent } from "@vue/composition-api";

export default defineComponent({
  name: "PageIndex",
  components: { ExampleComponent }
});
</script>
