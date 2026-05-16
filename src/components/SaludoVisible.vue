<template>
  <div>
    <p v-if="visible">¡Hola! Este mensaje aparece solo cuando el componente es visible en pantalla.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visible: true
    };
  }
};
</script>

