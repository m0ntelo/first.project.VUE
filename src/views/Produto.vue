<template>
  <section v-if="produto" class="produto">
    <p>Produto {{produto}}</p>
  </section>
</template>

<script>

import { api } from "@/services.js";

export default {
  name: "Produtos",
  props: ["id"],
  data() {
    return {
      produto: null
    }
  },
  methods: {
    getProduto() {
      api.get(`/produto/${this.id}`).then(response => {
        this.produto = response.data;
      });
    }
  },
  created() {
    this.getProduto();
  }
}
</script>

<style>

</style>