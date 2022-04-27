<script>
import { ref } from "vue";
import Vue from "vue";
import { vsButton, vsSelect, vsPopup } from "vuesax";

import "vuesax/dist/vuesax.css"; //Vuesax styles
Vue.use(vsButton);

const props = defineProps({
  count: {
    default: 0,
  },
});

const counter = ref(props.count);
export default {
  name: "Counter",
};
</script>

<template>
  <div flex="~" w="min" border="~ gray-400 opacity-50 rounded-md">
    <vs-button color="primary" type="filled">Primary</vs-button>
    <button
      border="r gray-400 opacity-50"
      p="2"
      font="mono"
      outline="!none"
      hover:bg="gray-400 opacity-20"
      @click="counter -= 1"
    >
      -
    </button>
    <span m="auto" p="2">{{ counter }}</span>
    <button
      border="l gray-400 opacity-50"
      p="2"
      font="mono"
      outline="!none"
      hover:bg="gray-400 opacity-20"
      @click="counter += 1"
    >
      +
    </button>
  </div>
</template>
