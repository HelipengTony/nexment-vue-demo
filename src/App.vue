<template>
  <div id="app">
    <NexmentContainer :config="configs" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import NexmentContainer from "nexment-vue";
import "nexment-vue/dist/nexment-vue.css";

Vue.use(NexmentContainer);

@Component
export default class App extends Vue {
  configs = {
    pageKey: "vueDemoPage",
    enableLinkInput: true,
    leancloud: {
      appId: "6Kcb9HB1iOR87HUbAvnMyUER-gzGzoHsz",
      appKey: "zf3gAf9CGIHLL8Crctb0sJLV",
      serverURL: "https://leancloud.ouorz.com",
    },
    admin: {
      name: "TonyHe",
      email: "he@holptech.com",
    },
  };
}
</script>

<style lang="scss">
body {
  margin: 0px;
}
@media screen and (min-width: 1000px) {
  #app {
    width: 650px !important;
    padding: 20px !important;
    border-left: 1px solid #eee;
    border-right: 1px solid #eee;
  }
}
#app {
  width: 100%;
  margin: 0 auto;
  padding: 0px;
}
</style>
