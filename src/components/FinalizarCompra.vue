<template>
  <section>
    <h2>Endereço de Envio</h2>
    <UsuarioForm>
      <button @click="finalizarCompra">Finalizar Compra</button>
    </UsuarioForm>
  </section>
</template>

<script>

import UsuarioForm from "@/components/UsuarioForm.vue";

export default {
  name: "FinalizarCompra",
  components: {
    UsuarioForm
  },
  props : ["produtos"]
}
</script>

<style>

</style>