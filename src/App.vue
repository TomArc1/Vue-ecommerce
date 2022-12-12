<template>
  <div id="app" class="bg-[#676767]">
    <site-header /> 
    <registro-cliente />
    <product-detail 
      :product= this.eldenRing 
    />
    <card-container />
    <my-cart />
  </div>
</template>

<script>
import SiteHeader from './components/SiteHeader.vue'
import RegistroCliente from './components/RegistroCliente.vue';
import CardContainer from './components/CardContainer.vue';
import ProductDetail from './components/ProductDetail.vue';
import MyCart from './components/MyCart.vue';

export default {
  name: 'App',

  components: {
    SiteHeader,
    RegistroCliente,
    CardContainer,
    ProductDetail,
    MyCart
  },

  data() {
    return {
      eldenRing:  {
        tipo: 'videojuego',
        id: '201',
        nombre: 'Elden Ring',
        desarrollador: 'From Software',
        precio: '70',
        genero: 'rol accion',
        modosDeJuego: 'Un jugador, multijugador',
        plataformas: 'Playstation 5, Playstation 4, PC, Xbox One, Xbox Series X/S',
        img: './imgs/eldenring.webp'
      },
    }
  }

}
</script>

