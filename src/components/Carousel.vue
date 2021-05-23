<template>
  <div style="padding-top: 50px;">
    <div :id="idCarousel" class="carousel slide" data-ride="carousel">
      <div class="carousel-inner">
        <div class="carousel-item active" >
          <CardProduto :produto="produtosExibidos[0]"></CardProduto>
          <CardProduto :produto="produtosExibidos[1]"></CardProduto>
          <CardProduto :produto="produtosExibidos[2]"></CardProduto>
        </div>
        <div class="carousel-item">
          <CardProduto :produto="produtosExibidos[3]"></CardProduto>
          <CardProduto :produto="produtosExibidos[4]"></CardProduto>
          
        </div>
      </div>
      <a
        class="carousel-control-prev"
        :href="hrefCarousel"
        role="button"
        data-slide="prev"
      >
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a
        class="carousel-control-next"
        :href="hrefCarousel"
        role="button"
        data-slide="next"
      >
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>
  </div>
</template>

<script>
import CardProduto from './CardProduto.vue'
export default {
  name: "Carousel",
  components: {
      CardProduto
  },
  props : {
      produtos: Array,
      id: Number
  },
  data() {
      return {
          produtosExibidos : this.produtos,
          idCarousel : "carouselExampleControls" + this.id,
          hrefCarousel : "#carouselExampleControls" + this.id
      }
  },
};
</script>

<style scoped>
.carousel-inner {
    width: 54rem;
}

.card {
    width: 18rem;
    height: 28rem;
    float: left;
}
</style>