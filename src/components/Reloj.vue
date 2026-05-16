<template>
  <div>
    <p>La hora actual es: {{ hora }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hora: new Date().toLocaleTimeString()
    };
  },
  mounted() {
    this.intervalo = setInterval(() => {
      this.hora = new Date().toLocaleTimeString();
    }, 1000);
  },
  beforeDestroy() {
    clearInterval(this.intervalo);
  }
};
</script>

