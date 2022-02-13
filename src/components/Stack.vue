<template>
  <div class="stack">
    <slot></slot>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  props: {
    space: {
      type: String,
      default: "3rem",
    },
  },
});
</script>

<style scoped>
.stack > ::v-slotted(* + *) {
  margin-top: v-bind(space);
}
</style>
