<template>
    <div class="w-full px-8 py-12 relative">
        <div class="rounded-xl bg-[#989898] pt-8 pb-28 px-8 w-full relative">
            <h3>Mis productos:</h3>
            <div class="flex justify-evenly bg-[#676767] rounded-t-xl">
                <p>ID</p>
                <p>Nombre</p>
                <p>Precio</p>
                <p>Unidades</p>
            </div>
            <div v-if="this.miCarro.length != [0]">
                <!-- <div v-for="(prod, idex) of micarro" :key="index">
    
                </div> -->
            </div>
            <div v-else>
                <div class="bg-white flex justify-center items-center py-12">
                    <div class="flex flex-col items-center">
                        <figure class="w-[18.75rem] h-[18.75rem]">
                            <img class="w-full h-full object-contain" src="/imgs/sadcarrito.jpeg" alt="coso">
                        </figure>
                        <p>Ey! acá no hay nada! </p>
                    </div>
                </div>
            </div>
    
            <button class="absolute bottom-8 left-[50%] translate-x-[-50%] text-white bg-orange-500 px-8 py-3 rounded-xl border border-white">Realizar compra</button>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            miCarro: [],
        }
    }
}
</script>