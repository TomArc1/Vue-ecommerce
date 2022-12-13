<template>
    <div class="px-8 py-16">
        <form ref="form" @submit.prevent="checkForm" class="w-[35rem] rounded-xl bg-[#989898] py-8 px-8 flex flex-col border border-white">
            <div>
                <div class="mb-4">
                    <label for="inputName" class="mr-6">Nombre:</label>
                    <input v-model="name" type="text" id="inputName" class="rounded-xl px-4 py-2 bg-[#eaeaea] outline-none" placeholder="Nombre completo">
                    <p v-show="nameWarning" class="text-red-600 text-xs">El ingreso debe ser nombre y apellido</p>
                </div>
                <div class="flex items-center mb-4">
                    <div>
                        <label for="inputName">Email:</label>
                        <input v-model="email1" type="email" id="inputEmail1" class="rounded-xl px-4 py-2 bg-[#eaeaea] outline-none" placeholder="ejemplo@ejemplo.com">
                        <p v-show="emailEmpty" class="text-red-600 text-xs">Completar email</p>
                        <p v-show="emailWarning" class="text-red-600 text-xs">El email debe ser el mismo</p>
                    </div>
                    <div>
                        <label for="inputName">Repetir email:</label>
                        <input v-model="email2" type="email" id="inputEmail2" class="rounded-xl px-4 py-2 bg-[#eaeaea] outline-none" placeholder="ejemplo@ejemplo.com">
                    </div>
                </div>
                <div class="flex items-center mb-4">
                    <div>
                        <label for="inputName">Clave</label>
                        <input v-model="password1" type="password" id="inputPassword1" class="rounded-xl px-4 py-2 bg-[#eaeaea] outline-none" placeholder="*******">
                        <p v-show="passwordEmpty" class="text-red-600 text-xs">Completar contraseñas</p>
                        <p v-show="passwordWarning" class="text-red-600 text-xs">La contraseña debe ser el mismo</p>
                    </div>
                    <div>
                        <label for="inputName">Repetir Clave</label>
                        <input v-model="password2" type="password" id="inputPassword2" class="rounded-xl px-4 py-2 bg-[#eaeaea] outline-none" placeholder="*******">
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
                        <input v-model="interests" type="checkbox" value="Xbox" id="checkXbox">
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
                <p v-show="interestsWarning" class="text-red-600 text-xs">Debes seleccional al menos 2 intereses</p>
                </div>
                
                <div class="mb-8">
                    <p class="form-check-label" for="checkNewsletter">
                        Queres recibir nuestros newsletters?
                    </p>
                    <div class="flex items-center justify-evenly">
                        <div class="col">
                            <input v-model="news" type="radio" name="checkNewsSi" value="Si">
                            <label for="checkDNI">Sí</label>
                        </div>
                        <div class="col">
                            <input v-model="news" type="radio" name="checkNewsno" value="No">
                            <label for="checkPass">No</label>
                        </div>
                    </div>
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
            nameOk: false,
            nameWarning: false,
            email1:'',
            email2:'',
            emailOk: false,
            emailEmpty: false,
            emailWarning: false,
            password1: '',
            password2: '',
            passwordOk: false,
            passwordEmpty: false, 
            passwordWarning: false,
            interests: [],
            interestsOk: false,
            interestsWarning: false,
            news: ''
      };
    },
    methods: {
        sendForm() {
            alert('Formulario enviado!')
            setTimeout(() => {
                this.$refs.form.reset()
                Object.assign(this.$data, this.$options.data());
            }, 100);
            return
        },

        checkName() {
            const checkName = this.name.trim().indexOf(' ');
            (checkName != -1) ? (this.nameOk = true) : (this.nameWarning = true)
        },

        checkEmail() {
            if(this.email1 != '' || this.email2 != '') {
                if (this.email1 === this.email2 ) {
                    this.emailEmpty = false
                    this.emailWarning = false
                    this.emailOk = true
                } else {
                    this.emailEmpty = false
                    this.emailOk = false
                    this.emailWarning = true
                }
            } else {
                this.emailWarning = false
                this.emailOk = false
                this.emailEmpty = true
            }

        },

        checkPass() {
            if (this.password1 != '' || this.password2 != '') {
                if  (this.password1 === this.password2) {
                    this.passwordEmpty = false
                    this.passwordWarning = false
                    this.passwordOk = true
                } else {
                    this.passwordEmpty = false
                    this.passwordOk = false
                    this.passwordWarning = true
                }
            } else {
                this.passwordOk = false
                this.passwordWarning = false
                this.passwordEmpty = true
            }
        },

        checkInterests() {
            if (this.interests.length >= 2) {
                this.interestsWarning = false
                this.interestsOk = true
                
            } else {
                this.interestsOk = false
                this.interestsWarning = true
            }
        },

        finalCheck () {
            if (this.nameOk && this.emailOk && this.passwordOk && this.interestsOk) {
                this.sendForm()
                console.log('final check ok')
            }
        },
        checkForm() {
            this.checkName();
            this.checkEmail();
            this.checkPass();
            this.checkInterests();
            this.finalCheck();
        },
    }

}

</script>