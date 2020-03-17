<template>
  <div id="app center">
    <h1>API Posts Vuex Axios</h1>
    <h2 v-for="(item, index) in posts" :key="index">
      {{ item.title }}
    </h2>
  </div>
</template>
<script>
import { mapState } from "vuex";
export default {
  name: "App",
  // data() {},
  mounted() {
    this.$store.dispatch("loadPosts");
  },
  computed: {
    ...mapState(["posts"])
  },
  components: {}
};
</script>
<style>
h1 {
  padding: 30px;
  text-align: center;
}
h2 {
  text-align: center;
}
</style>
