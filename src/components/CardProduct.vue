<template>
    <div class="w-[18rem] border flex flex-col items-center px-3 py-4 rounded-xl bg-[#989898]">
        <figure class="w-[16rem] h-[20rem] rounded-xl overflow-hidden mb-6">
            <img class="w-full h-full object-cover" :src="img" alt="coso">
        </figure>
        <h4 class="text- text-2xl">{{ nombre }}</h4>
        <div v-if="empresa">
            <p class="text-xs mb-4"> {{ empresa }} </p>
        </div>
        <div v-else-if="desarrollador">
            <p class="text-xs mb-4"> {{ desarrollador }} </p>
        </div>
        <p class="mb-4">$ {{ precio }}</p>
        <button class="text-white bg-orange-500 px-8 py-3 rounded-xl border border-white">Comprar</button>
    </div>
</template>

<script>
export default {
    props: {
        type: String,
        nombre: String,
        empresa: String,
        precio: String,
        desarrollador: String,
        portatil: String,
        color: String,
        fichaTecnica: String,
        modosDeJuego: String,
        plataforma: String,
        img: String,
    }
}
</script>