<template>
  <v-row class="mt-1" justify="center" align="center">
    <div class="mx-2 px-3" style="width: 100%;">
      <div class="mx-2 px-3" style="width: 100%;">
        <v-img class="banner" :src="require('/assets/images/banner.jpg')"></v-img>
      </div>
    </div>
    <v-row>
      <v-col cols="12" sm="6" lg="4">
        <div class="pa-5">
          <span class="font-weight-bold primary--text">
            BIENVENIDO AL CLUB SPORT SAN PABLO
          </span>
          <ul class="my-2">
            <li>
              <span class="font-weight-bold">País: </span> Paraguay
            </li>
            <li>
              <span class="font-weight-bold">Fecha de Fundacion: </span> 2022
            </li>
            <li>
              <span class="font-weight-bold">Disciplinas deportivas: </span> Futbol
            </li>
            <li>
              <span class="font-weight-bold">Sede: </span> Ypacarai
            </li>
          </ul>
          <span>
            Somos un equipo mixto de fútbol a quiénes nos encanta el fútbol y que disfrutamos con los amigos en este
            gran deporte que practicamos. Únete a nuestra aventura y ven a apoyarnos en todos los partidos que puedas.
          </span>
        </div>
      </v-col>
      <v-col cols="12" sm="6" lg="4">
        <div class="pa-5">
          <span class="font-weight-bold primary--text">
            SIGUENOS EN FACEBOOK
          </span>
          <div class="pt-2" style="max-height: 320px; height: 280px;">
            <iframe
              src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2FCSSP.42%2F%3Fhc_ref%3DARSIZoalM9UGm0AxZyyDS8dFQWf8VZjj9FLEeo0tul7g51ycHay96RtQfq4fmDQkfs0%26fref%3Dnf&tabs=timeline&width=340&height=500&small_header=false&adapt_container_width=true&hide_cover=false&show_facepile=true&appId=383753250443311"
              width="100%" height="100%" style="border:none;overflow:hidden" scrolling="no" frameborder="0"
              allowfullscreen="true"
              allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"></iframe>
          </div>
        </div>
      </v-col>
      <v-col cols="12" sm="6" lg="4">
        <div class="pa-5">
          <span class="font-weight-bold primary--text">
            NOTICIAS DEL CLUB
          </span>
          <div v-for="(publication, key) in publications" :key="key">
            <div class="hvr-grow publication">
              <NewsCard v-bind="publication" />
            </div>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-row>
</template>

<script>
import NewsCard from '~/components/Shared/NewsCard.vue';
export default {
  name: "IndexPage",
  data() {
    return {
      publications: [
        {
          image: require("/assets/images/footballnet4.jpg"),
          title: "Cadete campeon de liga",
          date: "- lunes 13 junio 2022"
        },
        {
          image: require("/assets/images/footballnet4.jpg"),
          title: "Cadete campeon de liga",
          date: "- lunes 13 junio 2022"
        },
        {
          image: require("/assets/images/footballnet4.jpg"),
          title: "Cadete campeon de liga",
          date: "- lunes 13 junio 2022"
        },
        {
          image: require("/assets/images/footballnet4.jpg"),
          title: "Cadete campeon de liga",
          date: "- lunes 13 junio 2022"
        },
      ],
      images: [
        require("/assets/images/banner.jpg"),
        require("/assets/images/sport-san-pablo-banner-2.jpg"),
        "https://www.holdsport.dk/media/W1siZiIsIjIwMjIvMDYvMDkvN2x0Yzl5MXNvdF9ncnVwb19kZV9uaW5fb3NfanVnYW5kb19mdV90Ym9sX2VuX3Nlc2lvX25fZW50cmVuYW1pZW50b191bl9jbHViX2Nvbl9jYW1pc2V0YXNfYXp1bGVzX3lfa2l0c19jaGljb3NfZmVsaWNlc19wcmFjdGljYW5kb19lbnRyZW5hZG9yXzIwODQ4MTQ4Ny5qcGciXSxbInAiLCJlbmNvZGUiLCJqcGciXV0/grupo-de-nin%CC%83os-jugando-fu%CC%81tbol-en-sesio%CC%81n-entrenamiento-un-club-con-camisetas-azules-y-kits-chicos-felices-practicando-entrenador-208481487.jpg?sha=68e46b93c994af48"
      ]
    };
  },
  methods: {
    menuItems() {
      return this.menu;
    }
  },
  components: { NewsCard }
}
</script>
<style>
.banner {
  border-bottom: solid;
  border-width: 0.4rem;
  border-color: #00aaff;
}

.publication:hover {
  cursor: pointer;
  border-bottom: solid;
  border-color: #00aaff;
  background-color: rgb(112, 112, 112, 0.1);
}
</style>