<template>
<div id="login">
        <div class="container">
            <div id="login-row" class="row justify-content-center align-items-center">
                <div id="login-column" class="col-md-6">
                    <div id="login-box" class="col-md-12">

                        <form id="login-form" class="form" action @submit="handleLoginForm">
                            <h3 class="text-center text-info unselectable">Iniciar sesión</h3>
                            <div class="form-group unselectable">
                                <label for="email" class="text-info unselectable">Correo electrónico:</label><br>
                                <input
                                    v-model="email"
                                    type="email"
                                    name="email"
                                    id="email"
                                    class="form-control"
                                    required
                                >
                            </div>
                            <div class="form-group unselectable">
                                <label for="password" class="text-info unselectable">Contraseña:</label><br>
                                <input
                                    v-model="password"
                                    type="password"
                                    name="password"
                                    id="password"
                                    class="form-control"
                                    required
                                >
                            </div>
                            <p v-if="error" class="unselectable">
                                <i class="fas fa-exclamation-triangle"></i>
                                Por favor, revisa tus credenciales.
                            </p>
                            <div class="form-group">
                                <!-- <label for="remember-me" class="text-info"><span>Remember me</span> <span><input id="remember-me" name="remember-me" type="checkbox"></span></label><br> -->
                                <input type="submit" name="submit" class="btn btn-info form-control" value="Ingresar">
                                <!-- <a href="#" class="text-info ml-4"> Register here</a> -->
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
        name: 'LoginScreen',
        data: () => ({
            email: '',
            password: ''
        }),
        methods: {
            handleLoginForm(e: Event) {
                e.preventDefault()
                console.log(`Hola, ${ this.email }`)
            }
        }
    });

</script>

<style scoped>

    #login .container #login-row #login-column #login-box {
        margin-top: 120px;
        max-width: 600px;
        height: 320px;
        /* border: 1px solid #9C9C9C; */
        /* background-color: #EAEAEA; */
    }
    #login .container #login-row #login-column #login-box #login-form {
        padding: 20px;
    }
    #login .container #login-row #login-column #login-box #login-form #register-link {
        margin-top: -85px;
    }

    .unselectable {
        user-select: none; /* standard syntax */
        -webkit-user-select: none; /* webkit (safari, chrome) browsers */
        -moz-user-select: none; /* mozilla browsers */
        -khtml-user-select: none; /* webkit (konqueror) browsers */
        -ms-user-select: none; /* IE10+ */
    }

</style>