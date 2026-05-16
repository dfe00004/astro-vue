<template>
  <form @submit.prevent="enviar">
    <label>
      Nombre:
      <input v-model="nombre" type="text" />
    </label>
    <button type="submit">Enviar</button>
    <div v-if="error" style="color:red">El nombre es obligatorio</div>
    <div v-if="enviado" style="color:green">¡Enviado!</div>
  </form>
</template>

<script>
export default {
  data() {
    return {
      nombre: '',
      error: false,
      enviado: false
    };
  },
  methods: {
    enviar() {
      this.error = false;
      this.enviado = false;
      if (!this.nombre) {
        this.error = true;
      } else {
        this.enviado = true;
        this.nombre = '';
      }
    }
  }
};
</script>
