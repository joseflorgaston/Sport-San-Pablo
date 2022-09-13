<template>
    <v-card class="mainNew">
        <v-card-title>
            <h3>CADETE CAMPEONES DE LA LIGA!</h3>
            <div class="d-flex justify-end" style="width: 100%;">
                <span class="grey--text caption font-italic">
                    lunes, 13 de junio de 2022 12:33:56 +0200
                </span>
            </div>
        </v-card-title>
        <div class="mb-2 px-3">
            <v-carousel v-model="model">
                <v-carousel-item v-for="(image, i) in images" :key="color">
                    <v-img
                        src="https://www.holdsport.dk/media/W1siZiIsIjIwMjIvMDYvMDkvN2x0Yzl5MXNvdF9ncnVwb19kZV9uaW5fb3NfanVnYW5kb19mdV90Ym9sX2VuX3Nlc2lvX25fZW50cmVuYW1pZW50b191bl9jbHViX2Nvbl9jYW1pc2V0YXNfYXp1bGVzX3lfa2l0c19jaGljb3NfZmVsaWNlc19wcmFjdGljYW5kb19lbnRyZW5hZG9yXzIwODQ4MTQ4Ny5qcGciXSxbInAiLCJlbmNvZGUiLCJqcGciXV0/grupo-de-nin%CC%83os-jugando-fu%CC%81tbol-en-sesio%CC%81n-entrenamiento-un-club-con-camisetas-azules-y-kits-chicos-felices-practicando-entrenador-208481487.jpg?sha=68e46b93c994af48">
                    </v-img>
                </v-carousel-item>
            </v-carousel>
        </div>
        <span class="px-3 py-3">
            Luego de un gran campeonato, nuestro Cadete se proclama campeón de liga provincial .
        </span>
    </v-card>
</template>
<script>
export default {
    data() {
        return {
            images: [
                require("/assets/images/footballnet4.jpg"),
                require("/assets/images/footballnet4.jpg"),
                require("/assets/images/footballnet4.jpg")
            ]
        }
    }
}
</script>