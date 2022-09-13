<template>
    <v-toolbar>
        <v-toolbar-title>
            <div class="d-flex py-2 align-items-center align-center ">
                <v-img lazy-src="https://picsum.photos/id/11/10/6" :src="require('/assets/images/logo.png')"
                    height="50px" width="50px"></v-img>
                <span class="d-none d-sm-flex font-weight-bold white--text pl-4">
                    CLUB SPORT SAN PABLO
                </span>
            </div>
        </v-toolbar-title>
        <v-spacer></v-spacer>
        <v-toolbar-items class="d-none d-md-flex">
            <v-btn v-for="item in menu" :key="item.icon" :to="item.link" active-class="active">
                {{item.title}}
            </v-btn>
        </v-toolbar-items>
        <div class="d-flex d-md-none">
            <div class="white-text">
                <v-menu>
                    <template v-slot:activator="{ on, attrs }">
                        <v-btn color="white" dark v-bind="attrs" v-on="on" icon>
                            <v-icon>mdi-menu</v-icon>
                        </v-btn>
                    </template>
                    <v-list>
                        <v-list-item v-for="(item, index) in menu" :key="index">
                            <v-btn :to="item.link" active-class="active">
                                {{item.title}}
                            </v-btn>
                        </v-list-item>
                    </v-list>
                </v-menu>
            </div>
        </div>
    </v-toolbar>
</template>
<script lang="ts">
import Vue from 'vue';
export default Vue.extend({
    name: "SharedHeader",
    data() {
        return {
            menu: [
                { icon: "home", title: "Inicio", link: "/" },
                { icon: "info", title: "Noticias", link: "/news" },
                { icon: "warning", title: "Contacto", link: "/contact" }
            ],
        }
    },
})
</script>