<template>
    <div id="register">
        <div class="container">
            <div id="register-row" class="row justify-content-center align-items-center">
                <div id="register-column" class="col-md-6">
                    <div id="register-box" class="col-md-12">
                        <form id="register-form" class="form" action @submit="handleRegisterForm">
                            <h3 class="text-center text-info">Registro</h3>
                            <div class="form-group">
                                <label for="#username" class="text-info">Nombre:</label><br>
                                <input
                                    v-model="username"
                                    type="text"
                                    name="username"
                                    id="username"
                                    class="form-control"
                                    required
                                >
                            </div>
                            <div class="form-group">
                                <label for="#email" class="text-info">Correo electrónico:</label><br>
                                <input
                                    v-model="email"
                                    type="text"
                                    name="email"
                                    id="email"
                                    class="form-control"
                                    required
                                >
                            </div>
                            <div class="form-group">
                                <label for="#password" class="text-info">Contraseña:</label><br>
                                <input
                                    v-model="password"
                                    type="password"
                                    name="password"
                                    id="password"
                                    class="form-control"
                                    required
                                >
                            </div>
                            <div class="form-group">
                                <label for="#passwordRepeat" class="text-info">Repita su contraseña:</label><br>
                                <input
                                    v-model="passwordRepeat"
                                    type="password"
                                    name="passwordRepeat"
                                    id="passwordRepeat"
                                    class="form-control"
                                    required
                                >
                            </div>
                            <div class="form-group">
                                <!-- <label for="remember-me" class="text-info"><span>Remember me</span> <span><input id="remember-me" name="remember-me" type="checkbox"></span></label><br> -->
                                <input
                                    type="submit"
                                    name="submit"
                                    class="btn btn-success form-control"
                                    value="Crear cuenta"
                                />
                                <!-- <a href="#" class="text-info ml-4"> Register here</a> -->
                            </div>
                            <div id="register-link" class="text-right">
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">

    import { defineComponent } from 'vue';

    export default defineComponent({
        name: 'RegisterScreen',
        data: () => ({
            username: '',
            email: '',
            password: '',
            passwordRepeat: '',
        }),
        methods: {
            handleRegisterForm(e: Event) {
                e.preventDefault();
                console.log(`Hola ${ this.username }`)
            }
        }
    });

</script>

<style scoped>

    #register .container #register-row #register-column #register-box {
        margin-top: 120px;
        max-width: 600px;
        height: 320px;
        /* border: 1px solid #9C9C9C; */
        /* background-color: #EAEAEA; */
    }
    #register .container #register-row #register-column #register-box #register-form {
        padding: 20px;
    }
    #register .container #register-row #register-column #register-box #register-form #register-link {
        margin-top: -85px;
    }

</style>
