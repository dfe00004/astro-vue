<template>
  <div>
    <p v-if="esMovil">¡Estas en un dispositivo movil!</p>
    <p v-else>¡No estas en un dispositivo movil!</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      esMovil: false
    };
  },
  mounted() {
    this.esMovil = window.matchMedia('(max-width: 600px)').matches;
  }
};
</script>

