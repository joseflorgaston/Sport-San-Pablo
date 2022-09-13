<template>
  <v-row class="mt-1" justify="center" align="center">
    <div class="mx-2 px-3" style="width: 100%;">
      <v-img class="banner" :src="require('/assets/images/banner.jpg')"></v-img>
    </div>
    <v-row>
      <v-col cols="12" sm="6" lg="4">
        <WelcomeDescription class="pt-5 px-6" />
      </v-col>
      <v-col cols="12" sm="6" lg="4">
        <FacebookIframe class="pa-5"/>
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
import WelcomeDescription from '~/components/Index/WelcomeDescription.vue';
import FacebookIframe from '~/components/Index/FacebookIframe.vue';
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
    };
  },
  methods: {
    menuItems() {
      return this.menu;
    }
  },
  components: { NewsCard, WelcomeDescription, FacebookIframe }
}
</script>
<style>
.banner {
  border-bottom: solid;
  border-width: 0.4rem;
  border-color: #00aaff;
  width: 100%;
}

.publication:hover {
  cursor: pointer;
  border-bottom: solid;
  border-color: #00aaff;
  background-color: rgb(112, 112, 112, 0.1);
}
</style>