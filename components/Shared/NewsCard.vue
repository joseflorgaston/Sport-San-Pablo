<template>
    <div class="d-flex mt-2">
        <div class="portada">
            <v-img :src="image" height="55px" width="80px"></v-img>
        </div>
        <div class="px-2">
            <div>
                <span class="font-weight-bold white--text">
                    {{title}}
                </span>
            </div>
            <div class="d-flex font-weight-bold grey--text" style="font-size: 12px;">
                <v-icon small color="grey">mdi-calendar</v-icon>
                {{date}}
            </div>
            <div class="grey--text" style="font-size: 12px;">12:33:30 +0200</div>
        </div>
    </div>
</template>
<script lang="ts">
import Vue from 'vue';
export default Vue.extend({
    name: "NewsCard",
    props: {
        image: {
            type: String,
            required: true
        },
        title: {
            type: String,
            required: true
        },
        description: {
            type: Array,
            required: false
        },
        date: {
            type: String,
            required: true
        }
    },
})
</script>