<template>
  <v-app dark>
    <v-container class="max-width">
      <v-card>
        <SharedHeader />
        <Nuxt />
      </v-card>
    </v-container>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';
import SharedHeader from '../components/Shared/SharedHeader.vue';
export default Vue.extend({
  name: "DefaultLayout",
  components: { SharedHeader }
})
</script>
<style>
body {
  overflow: hidden;
}

.max-width {
  max-width: 1200px;
  width: 100%;
}

.active {
  border-bottom: solid;
  border-color: #00aaff;
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