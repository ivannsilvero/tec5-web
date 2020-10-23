<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <router-link to="/" class="navbar-brand">
            <img style="height: 40px;" src="./eestn5.jpeg" alt=""/>
        </router-link>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav mr-auto">
                <!-- <li class="nav-item">
                    <router-link to="/notas" class="nav-link">
                        Mi Cuaderno
                    </router-link>
                </li> -->
            </ul>
            <span>

            </span>

            <router-link to="/profile" class="my-profile rl-wod">
                <img src="./yo.jpg" class="circle" />
                Ivan
            </router-link>

            <router-link to="/notas" class="my-profile rl-wod ml-3">
                <span class="fa-stack fa-lg">
                    <i class="fa fa-circle fa-stack-2x"></i>
                    <i class="fa fa-book fa-stack-1x"></i>
                </span>
            </router-link>

            <router-link to="/compose" class="my-profile rl-wod ml-3">
                <span class="fa-stack fa-lg">
                    <i class="fa fa-circle fa-stack-2x"></i>
                    <i class="fas fa-feather fa-stack-1x"></i>
                </span>
            </router-link>

        </div>
    </nav>
</template>

<script lang="ts">

    import { defineComponent } from 'vue'

    export default defineComponent({
        name: 'Navbar',
    });

</script>

<style scoped>

    nav {
        user-select: none; /* standard syntax */
        -webkit-user-select: none; /* webkit (safari, chrome) browsers */
        -moz-user-select: none; /* mozilla browsers */
        -khtml-user-select: none; /* webkit (konqueror) browsers */
        -ms-user-select: none; /* IE10+ */
    }

    .my-profile {
        border-radius: 18px;
        cursor: pointer;
        padding: 2px;
    }

    .circle {
        border-radius: 100%;
        height: 40px;
        width: 40px;
        border-radius: 50%;
        padding: 1px;
    }

    .my-profile:hover {
        background-color: gray;
    }


    .rl-wod {
        color: inherit;
        text-decoration: none;
    }

    .fa-circle {
        color: #f8f9fa;
    }

    .fa-lg:hover {
        /* color: rgba(0, 0, 0, 0.8); */
        color: blue;
    }

    .fa-circle:hover {
        color: gray;
    }

    .fa-book {
        position: relative;
        z-index: 99;
    }

</style>