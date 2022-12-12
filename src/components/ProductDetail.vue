<template>
    <div class="w-full mb-40">
        <div class="flex justify-center">
            <div class="flex items-center border rounded-xl p-9 bg-[#989898]">
                <div class="w-[20rem] h-full flex justify-center items-center bg-white rounded-xl mr-8">
                    <figure class="w-[10rem] h-[15rem]">
                        <img class="w-full h-full object-contain" :src="product.img" alt="coso">
                    </figure> 
                </div>
                <div class="flex flex-col items-start max-w-[25rem]">
                    <div class="flex flex-col mb-12">
                        <p class="text-3xl">{{ product.nombre }}</p>
                        <p class="text-xs">ID: {{ product.id }} </p>
                        <p class="text-xs">Desarrolladora: {{ product.desarrollador }} </p>
                        <p class="text-xs">Plataformas: {{ product.plataformas }} </p>
                        <p class="text-xs">Modos de Juego: {{ product.modosDeJuego }} </p>
                    </div>
                    <button class="text-white bg-orange-500 px-8 py-3 rounded-xl border border-white">Lo quiero!</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
    props: {
        product: Object
    }

}
</script>