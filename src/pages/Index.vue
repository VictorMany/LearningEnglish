<template>
  <q-page class="row items-center justify-evenly">
    <example-component
      title="Example component"
      active
    ></example-component>
  </q-page>
</template>

<script lang="ts">
import ExampleComponent from "components/CompositionComponent.vue";
import { defineComponent, ref } from "@vue/composition-api";

export default defineComponent({
  name: "PageIndex",
  components: { ExampleComponent }
});
</script>
