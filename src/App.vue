<template>
  <AlertProvider msg="button">
    <template #default="{ on, clicked }">
      <button v-on="on">Click me</button>
      <div v-if="clicked">has clicked button !!</div>
    </template>
  </AlertProvider>
  <AlertProvider msg="div">
    <template #default="{ on, clicked }">
      <div v-on="on">Click me</div>
      <div v-if="clicked">has clicked div !!</div>
    </template>
  </AlertProvider>
</template>

<script lang="ts">
import { defineComponent } from "vue"
import AlertProvider from "./components/AlertProvider.vue"
export default defineComponent({
  components: {
    AlertProvider,
  },
})
</script>
