<template>
  <v-app dark>
    <v-container class="max-width">
      <v-card>
        <v-toolbar>
          <v-toolbar-title>
            <div class="d-flex py-2 align-items-center align-center ">
              <v-img lazy-src="https://picsum.photos/id/11/10/6" :src="require('/assets/images/logo.png')" height="50px"
                width="50px"></v-img>
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
        <Nuxt />
      </v-card>
    </v-container>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
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
body {
  overflow: hidden;
}

.max-width {
  max-width: 1200px;
  width: 100%;
}

.hvr-grow {
  display: inline-block;
  vertical-align: middle;
  transform: translateZ(0);
  box-shadow: 0 0 1px rgba(0, 0, 0, 0);
  backface-visibility: hidden;
  -moz-osx-font-smoothing: grayscale;
  transition-duration: 0.3s;
  transition-property: transform;
}

.hvr-grow:hover,
.hvr-grow:focus,
.hvr-grow:active {
  transform: scale(1.1);
}

.hvr-skew {
  display: inline-block;
  vertical-align: middle;
  -webkit-transform: perspective(1px) translateZ(0);
  transform: perspective(1px) translateZ(0);
  box-shadow: 0 0 1px rgba(0, 0, 0, 0);
  -webkit-transition-duration: 0.3s;
  transition-duration: 0.3s;
  -webkit-transition-property: transform;
  transition-property: transform;
}

.hvr-skew:hover,
.hvr-skew:focus,
.hvr-skew:active {
  -webkit-transform: skew(-10deg);
  transform: skew(-10deg);
}
</style>