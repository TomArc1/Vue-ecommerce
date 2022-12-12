<template>
    <div class="px-8 py-16">
        <form ref="form" class="w-[35rem] rounded-xl bg-[#989898] py-8 px-8 flex flex-col border border-white">
            <div>
                <div class="mb-4">
                    <label for="inputName" class="mr-6">Nombre:</label>
                    <input v-model="name" type="text" id="inputName" class="rounded-xl px-4 py-2 bg-[#eaeaea] outline-none" placeholder="Nombre completo">
                </div>
                <div class="flex items-center mb-4">
                    <div>
                        <label for="inputName">Email:</label>
                        <input v-model="email" type="email" id="inputName" class="rounded-xl px-4 py-2 bg-[#eaeaea] outline-none" placeholder="ejemplo@ejemplo.com">
                    </div>
                    <div>
                        <label for="inputName">Repetir email:</label>
                        <input v-model="email2" type="email" id="inputName" class="rounded-xl px-4 py-2 bg-[#eaeaea] outline-none" placeholder="ejemplo@ejemplo.com">
                    </div>
                </div>
                <div class="flex items-center mb-4">
                    <div>
                        <label for="inputName">Clave</label>
                        <input v-model="email2" type="password" id="inputName" class="rounded-xl px-4 py-2 bg-[#eaeaea] outline-none" placeholder="*******">
                    </div>
                    <div>
                        <label for="inputName">Repetir Clave</label>
                        <input v-model="email2" type="password" id="inputName" class="rounded-xl px-4 py-2 bg-[#eaeaea] outline-none" placeholder="*******">
                    </div>  
                </div>
                <div class="flex flex-wrap max-w-[20rem] my-6">
                    <div class="mb-2 mx-6">
                        <input v-model="interests" type="checkbox" value="Consolas" id="checkConsolas">
                        <label class="form-check-label" for="checkConsolas">
                            Consolas
                        </label>
                    </div>
                    <div class="mb-2 mx-6">
                        <input v-model="interests" type="checkbox" value="Videojuegos" id="checkVideojuegos">
                        <label class="form-check-label" for="checkVideojuegos">
                            Videojuegos
                        </label>
                    </div>
                    <div class="mb-2 mx-6">
                        <input v-model="interests" type="checkbox" value="Noticias" id="checkNoticias">
                        <label class="form-check-label" for="checkNoticias">
                            Noticias
                        </label>
                    </div>
                    <div class="mb-2 mx-6">
                        <input v-model="interests" type="checkbox" value="Ofertas" id="checkOfertas">
                        <label class="form-check-label" for="checkOfertas">
                            Ofertas
                        </label>
                    </div>
                    <div class="mb-2 mx-6">
                        <input v-model="interests" type="checkbox" value="Consolas" id="checkXbox">
                        <label class="form-check-label" for="checkXbox">
                            Xbox
                        </label>
                    </div>
                    <div class="mb-2 mx-6">
                        <input v-model="interests" type="checkbox" value="Nintendo" id="checkNintendo">
                        <label class="form-check-label" for="checkNintendo">
                            Nintendo
                        </label>
                    </div>
                    <div class="mb-2 mx-6">
                        <input v-model="interests" type="checkbox" value="Playstation" id="checkPlaystation">
                        <label class="form-check-label" for="checkPlaystation">
                            Playstation
                        </label>
                    </div>
                </div>
                <div class="mb-8">
                    <input v-model="news" type="checkbox" value="Playstation" id="checkPlaystation">
                    <label class="form-check-label" for="checkPlaystation">
                        Queres recibir nuestros newsletters?
                    </label>
                </div>
            </div>
            <button class="w-fit mx-auto text-white bg-orange-500 px-8 py-3 rounded-xl border border-white">Registrarse</button>
        </form>
    </div>
</template>

<script>

export default {
    name: 'RegistroCliente',
    
    data() {
      return {
            name: '',
            email:'',
            email2:'',
            password: '',
            password2: '',
            interests: [],
            news: false
      };
    }

}

</script>