<template>
    <q-layout view="hHh lpr lfr">
        <q-header elevated>
            <q-toolbar>
                <q-avatar size="30px">
                    <img :src="url" />
                </q-avatar>

                <q-toolbar-title>
                    {{ appTitle }}
                </q-toolbar-title>

                <div class="q-pa-xs q-gutter-xs">
                    <q-btn to="/" flat label="Inicio" />
                    <q-btn to="/about" flat label="Sobre" />
                </div>
            </q-toolbar>
        </q-header>
        <q-page-container>
            <router-view />
        </q-page-container>
    </q-layout>
</template>

<script>
export default {
    name: "MainLayout",

    data() {
        return {
            url: "./src/assets/icon-256-light.png",
            appTitle: "Quasar Todo",
        };
    },
};
</script>
