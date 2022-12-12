<template>
    <div class="flex items-center relative">
        <div v-show="data" class="flex items-center">
            <div class="flex items-center">
                <input @v-model="usuario" id="inputUsuario" class="rounded-xl px-4 py-2 bg-[#eaeaea] outline-none" type="text" placeholder="usuario">
            </div>
            <div class="flex items-center ml-3">
                <input @v-model="contrasena" id="inputContrasena" class="rounded-xl px-4 py-2 bg-[#eaeaea] outline-none" type="text" placeholder="contraseña">
            </div>
            <button @click="check" class="text-white bg-orange-500 px-8 py-2 rounded-xl border border-white mx-4">Ingresar</button>
        </div>
        <p v-show="alert" class="absolute top-[3rem] text-red text-xs">Falta ingresar datos</p>
        <p v-show="welcome" class="mr-16">Bienvenido {{ usuario }}</p>
    </div>
</template>

<script>

export default {

    data(){
        return {   
            usuario: '',
            contrasena: '',
            welcome: false,
            alert: false,
            data: true,
        }
    },

    methods: {
        check() {
            if(this.usuario === '' && this.contrasena === '') {
                this.alert = true
                return
            }
            this.alert = false
            this.data = false
            this.welcome = true
        }
    }

}

</script>