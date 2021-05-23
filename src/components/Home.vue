<template>
  <div class="wrapper">
    <NavBar></NavBar>
    <div class="row d-flex justify-content-center" id="secao-pesquisa">
      <SearchBar></SearchBar>
    </div>
    
    <div class="row d-flex justify-content-center" id="secao-produtos">
      <Carousel :produtos="notebooks" :id=1></Carousel>
      <Carousel :produtos="ssds" :id=2></Carousel>
    </div>
    


    <Footer></Footer>
  </div>
</template>

<script>
import SearchBar from "./SearchBar.vue";
import NavBar from "./NavBar.vue";
import Footer from "./Footer.vue";
import Carousel from "./Carousel.vue";
export default {
  name: "Home",
  components: {
    SearchBar,
    NavBar,
    Footer,
    Carousel
  },

  data() {
    return {
      notebooks : [
        {
          nome: 'Notebook Samsung',
          preco: '2499,99',
          imagem: 'images/produtos/notebooks/notebook1.jpg'

        },
        {
          nome: 'Notebook Acer',
          preco: '1899,99',
          imagem: 'images/produtos/notebooks/notebook2.jpg'

        },
        {
          nome: 'Notebook Lenovo',
          preco: '2299,99',
          imagem: 'images/produtos/notebooks/notebook3.jpg'

        },
        {
          nome: 'Notebook LG',
          preco: '1999,99',
          imagem: 'images/produtos/notebooks/notebook4.jpg'

        },
        {
          nome: 'Notebook Dell',
          preco: '2999,99',
          imagem: 'images/produtos/notebooks/notebook5.jpg'

        }
      ],
      ssds : [
        {
          nome: 'SSD Kingston 240GB',
          preco: '199,99',
          imagem: 'images/produtos/ssds/ssd1.jpg'

        },
        {
          nome: 'SSD WM 128GB',
          preco: '129,99',
          imagem: 'images/produtos/ssds/ssd2.jpg'

        },
        {
          nome: 'SSD WD 240GB',
          preco: '179,99',
          imagem: 'images/produtos/ssds/ssd3.jpg'

        },
        {
          nome: 'SSD WD M.2 2280 240GB',
          preco: '169,99',
          imagem: 'images/produtos/ssds/ssd4.jpg'

        },
        {
          nome: 'SSD Crucial 120GB',
          preco: '139,99',
          imagem: 'images/produtos/ssds/ssd5.jpg'

        }
      ]
    }
  },
};
</script>

<style scoped>
.wrapper{
    margin-top: 0;
    background: #393E46;
}
#secao-produtos {
    background: #545c68;
}
</style>