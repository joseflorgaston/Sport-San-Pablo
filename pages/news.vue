<template>
    <div class="d-flex flex-wrap justify-center pa-3">
        <div>
            <h1>Noticias del club</h1>
        </div>
        <div style="width:100%">
            <v-row>
                <v-col cols="12" md="8">
                    <MainNewCard />
                </v-col>
                <v-col cols="12" md="4">
                    <div v-for="(publication, key) in publications" :key="key">
                        <div class="hvr-grow publication">
                            <NewsCard v-bind="publication" />
                        </div>
                    </div>
                </v-col>
            </v-row>
        </div>
    </div>
</template>
<script lang="ts">
import Vue from 'vue';
import NewsCard from '~/components/Shared/NewsCard.vue';
import MainNewCard from '~/components/News/MainNewCard.vue';
export default Vue.extend({
    components: { NewsCard, MainNewCard },
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
                {
                    image: require("/assets/images/footballnet4.jpg"),
                    title: "Cadete campeon de liga",
                    date: "- lunes 13 junio 2022"
                },
            ],
        };
    },
})
</script>
<style scoped>
.mainNew {
    background-color: #272727;
}
</style>