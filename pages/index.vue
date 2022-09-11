<template>
  <v-row class="mt-2" justify="center" align="center">
    <v-card class="d-flex flex-wrap justify-center max-width">
      <v-toolbar>
        <v-toolbar-title>
          <div class="d-flex py-2 align-items-center align-center ">
            <v-img :src="require('/assets/images/logo.png')" height="50px" width="50px"></v-img>
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
                <v-btn color="primary" dark v-bind="attrs" v-on="on">
                  Dropdown
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
      <div class="banner">
        <v-img :src="require('/assets/images/banner.jpg')"></v-img>
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
              <div id="fb-root"></div>
              <iframe
                src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2Fpablitojere&tabs=timeline&width=340&height=500&small_header=false&adapt_container_width=true&hide_cover=false&show_facepile=true&appId=383753250443311"
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
              <div class="d-flex mt-2 hvr-grow publication">
                <div class="portada">
                  <v-img :src="publication.image" height="55px" width="80px"></v-img>
                </div>
                <div class="px-2">
                  <div>
                    <span class="font-weight-bold white--text">
                      {{publication.title}}
                    </span>
                  </div>
                  <div class="d-flex font-weight-bold grey--text" style="font-size: 12px;">
                    <v-icon small color="grey">mdi-calendar</v-icon>
                    {{publication.date}}
                  </div>
                  <div class="grey--text" style="font-size: 12px;">12:33:30 +0200</div>
                </div>
              </div>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-card>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      publications: [
        {
          image: require('/assets/images/footballnet4.jpg'),
          title: "Cadete campeon de liga",
          date: "- lunes 13 junio 2022"
        },
        {
          image: require('/assets/images/footballnet4.jpg'),
          title: "Cadete campeon de liga",
          date: "- lunes 13 junio 2022"
        },
        {
          image: require('/assets/images/footballnet4.jpg'),
          title: "Cadete campeon de liga",
          date: "- lunes 13 junio 2022"
        },
        {
          image: require('/assets/images/footballnet4.jpg'),
          title: "Cadete campeon de liga",
          date: "- lunes 13 junio 2022"
        },
      ],
      clipped: false,
      drawer: false,
      fixed: false,
      menu: [
        { icon: "home", title: "Inicio", link: "/" },
        { icon: "info", title: "Noticias", link: "/news" },
        { icon: "warning", title: "Contacto", link: "/contact" }
      ],
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
    }
  },
  methods: {
    menuItems() {
      return this.menu;
    }
  }
}
</script>
<style>
.max-width {
  max-width: 1200px;
  width: 100%;
}

.banner {
  border-bottom: solid;
  border-width: 0.4rem;
  border-color: #00aaff;
  width: 100%;
}

.active {
  border-bottom: solid;
  border-color: #00aaff;
}

.publication:hover {
  cursor: pointer;
  border-bottom: solid;
  border-color: #00aaff;
  background-color: rgb(112, 112, 112, 0.1);
}
</style>