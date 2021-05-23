<template>
  <div class="card">
    <div class="card-imagem">
      <img class="card-img-top" :src="imagemProd" alt="Card image cap" />
    </div>

    <div class="card-body">
      <h5 class="card-title">{{nomeProd}}</h5>
      <p class="card-text">{{precoProd}}</p>
      <a href="#" class="btn btn-primary">Comprar</a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    produto: Object,
  },

  data() {
    return {
      nomeProd: this.produto.nome,
      precoProd: this.produto.preco,
      imagemProd: this.getImgUrl(this.produto.imagem),
    };
  },
  methods: {
    getImgUrl(pic) {
      return require("../assets/" + pic);
    },
  },
};
</script>

<style scoped>
.card {
  width: 18rem;
  height: 28rem;
  float: left;
}
</style>