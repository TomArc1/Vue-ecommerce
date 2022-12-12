<template>
    <div class="w-full flex justify-between items-center bg-white px-8 py-8">  
        <p class="">Aca irá algún logo, algún día, tal vez.</p>
        <div class="flex items-center">
          <ingreso-cliente/>
          <!-- Link al carrito -->
          <div class="relative">
            <a href="#" class="absolute z-1">
              <figure class="w-8 h-8">
                  <img class="w-full h-full object-cover" src="/imgs/carrito.png" alt="carrito">
              </figure>
            </a>
            <div class="relative z-2 top-4 left-4 w-6 h-6 bg-red-600 text-white flex items-center justify-center rounded-full">1</div>
          </div>
        </div>
    </div>
</template>

<script>
import IngresoCliente from './IngresoCliente.vue';

export default {
  name: 'SiteHeader',
  components: {
    IngresoCliente
  }
}
</script>

