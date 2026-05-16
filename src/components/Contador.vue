<template>
  <button @click="contador++">Has hecho clic {{ contador }} veces</button>
</template>

<script>
export default {
  data() {
    return {
      contador: 0
    };
  }
};
</script>

