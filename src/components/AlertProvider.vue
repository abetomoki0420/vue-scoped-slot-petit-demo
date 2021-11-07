<template>
  <slot :on="{ click: show }" :clicked="clicked" />
</template>

<script lang="ts">
import { ref } from "vue"
import { defineComponent } from "vue"
export default defineComponent({
  props: {
    msg: {
      type: String,
      default: "",
      required: false,
    },
  },
  setup(props) {
    const clicked = ref(false)

    const show = () => {
      clicked.value = true
      alert(props.msg)
    }
    return {
      clicked,
      show,
    }
  },
})
</script>
