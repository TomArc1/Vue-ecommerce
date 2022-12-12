<template>
    <div class="grid grid-cols-4 gap-4 px-8">
        <div v-for="(prod, index) in stock" :key="index">
            <card-product 
                :id="prod.id" 
                :nombre="prod.nombre" 
                :empresa="prod.empresa"
                :desarrollador="prod.desarrollador"
                :precio="prod.precio"
                :img="prod.img"
            />
        </div>

    </div>
</template>


<script>
import CardProduct from './CardProduct.vue';

export default {
    name: 'CardContainer',

    components: {
        CardProduct
    },

    data() {
        return {
        stock: [
            {
                tipo: 'consola',
                id: '101',
                nombre: 'PlayStation 5',
                empresa: 'Sony',
                precio: '500',
                portatil: 'No',
                color: 'Blanco',
                fichaTecnica: 'muchas cosas',
                img: './imgs/play.webp'
            },
            {
                tipo: 'consola',
                id: '102',
                nombre: 'Nintendo Switch',
                empresa: 'Nintendo',
                precio: '500',
                portatil: 'Si',
                color: 'Azul, Negro, Rojo',
                fichaTecnica: 'muchas cosas',
                img: './imgs/nintendo.webp'
            },
            {
                tipo: 'consola',
                id: '103',
                nombre: 'Xbox Series X',
                empresa: 'Microsoft',
                precio: '500',
                portatil: 'No',
                color: 'Negro',
                fichaTecnica: 'muchas cosas',
                img: './imgs/xbox.webp'
            },
            {
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
            {
                tipo: 'videojuego',
                id: '202',
                nombre: 'The Last of Us Part II',
                desarrollador: 'Naughty Dog',
                precio: '70',
                genero: 'terror, accion-aventura, shooter',
                modosDeJuego: 'Un jugador',
                plataformas: 'Playstation 5, Playstation 4',
                img: './imgs/tlou2.webp'
            },
            {
                tipo: 'videojuego',
                id: '203',
                nombre: 'Bayonetta 3',
                desarrollador: 'PlatinumGames',
                precio: '70',
                genero: 'Hack and slash, Acción',
                modosDeJuego: 'Un jugador',
                plataformas: 'Nintendo Switch',
                img: './imgs/bayonetta.webp'
            },
            {
                tipo: 'videojuego',
                id: '204',
                nombre: 'Hades',
                desarrollador: 'Supergiant Games',
                precio: '70',
                genero: 'Roguelite',
                modosDeJuego: 'Un jugador',
                plataformas: 'Nintendo Switch, Microsoft, macOS, Playstation, Xbox',
                img: './imgs/hades.webp'
            },
        ]
        }
  }
}
</script>